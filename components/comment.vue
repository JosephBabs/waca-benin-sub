<template>
    <div>
        <div class="comment-one" v-for="comment in comments" :key="comment.id">
              <h3 class="comment-one__title">{{comment.comments_count}} Comments</h3> 
              <div class="comment-one__single">
                <div class="comment-one__image">
                  <img src="/assets/images/blog/comment-1-1.png" alt="">
                </div>
                <div class="comment-one__content">
                  <h3>{{comment.fullname}}</h3>
                  <p> {{comment.comment_description}}</p>
                  <!-- <a href="#" class="thm-btn comment-one__btn">Reply</a> -->
                </div>
              </div>
            </div>

            <div class="comment-form">
      <h3 class="comment-form__title">Laissez un commentaire</h3>
      <form @submit.prevent="submitData" class="comment-one__form contact-form-validated">
        <!-- handleSubmit -->
        <div class="row">
          <div class="col-xl-6">
            <div class="comment-form__input-box">
              <input type="text" placeholder="Votre nom" v-model="form.fullname" name="name" />
            </div>
          </div>
          <div class="col-xl-6">
            <div class="comment-form__input-box">
              <input type="email" placeholder="Email" v-model="form.email" name="email" />
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-xl-12">
            <div class="comment-form__input-box">
              <textarea name="message" v-model="form.comment_description" placeholder="Saisir le message"></textarea>
            </div>
            <UAlert title="Hello"/>
            <button type="submit" class="thm-btn comment-form__btn">
              <i class="fas fa-arrow-circle-right"></i>Envoyer le Commentaire
            </button>
          </div>
        </div>
      </form>
    
      <div class="alert success-a" v-if="showAlert_s">
       Commentaire envoyé</div>

       <div class="alert danger-a" v-if="showAlert_d">
       Erreur: vérifiez votre connexion</div>
      
    
    </div>
    </div>
</template>


<script>

moment().format();
// const toasts = ;
 function showAlert(){
  setTimeout(() => {
    const elements = document.getElementsByClassName("alert");
    for (let i = 0; i < elements.length; i++) {
        elements[i].style.display = "none";
    }
}, 3000);

 }

async function postData(url, data) {
  try {
    const response = await fetch(url, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify(data),
    });

    if (!response.ok) {
      throw new Error('Network response was not ok');
      alert("Erreur de connexion")
    }

    const result = await response.json();
    return result;
  } catch (error) {
    console.error('Error:', error);
    throw error;
  }
};


  export default {
    
    data() {
    return {
      comments: [],

      form: {
          
          fullname: "", 
          email: "",
          comment_description: "",
        },
      showAlert_s: false, // Initially, hide the alert
      showAlert_d: false, // Initially, hide the alert
      alertType: '',    // Type of the alert ('success' or 'error')
      alertMessage: '', // Message to display in the alert
    
    };
  },
  name: 'ContactForm',
    
  methods: {

    
      async getData() {
        const apiLink = dataT.apiUrl.link;
        const res = await fetch("https://app.cmabenin.bj/api/posts/"+this.$route.query.post);
        const finalRes = await res.json();
        // console.log(finalRes.post);
        // alert(apiLink + 'post/')
        this.comments = finalRes.comments;
      },
     calcDate(date) {
      let nowDate = moment();
      // let pickDate = moment(date.toString(), 'YYYY-MM-DD-SS');
      
    let dateDiff = moment.duration(nowDate.diff(date));
      
    switch (true) {
        case dateDiff.asSeconds() < 60:
            return "à l'instant";
        case dateDiff.asMinutes() < 60:
            return dateDiff.minutes() + ' min';
        case dateDiff.asHours() < 24:
            return dateDiff.hours() + ' hr(s)';
        case dateDiff.asDays() < 30:
            return dateDiff.days() + ' jr(s)';
        case dateDiff.asMonths() < 12:
            return dateDiff.months() + ' mois';
        default:
            return dateDiff.years() + ' an(s)';
    }

    
      },
   



      // skyned

      
      // Example usage in a component
  async  submitData() {
  const apiLink = dataT.apiUrl.link;
  const url = apiLink+'comments';
  const data = {
    
    post_id : this.$route.query.post,
    fullname: this.form.fullname, 
    email: this.form.email,
    comment_description: this.form.comment_description ,
          
  };

  try {
    const response = await postData(url, data);
    console.log('Response:', response);
    this.showAlert_s = true;
    //     this.alertType = 'success';
    //     this.alertMessage = 'Commentaire envoyé';
    
    this.comments.push(this.form)
    showAlert()
    
    // alert("Commentaire envoyé")

    
    // Handle the response data here
  } catch (error) {
    console.error('Error:', error);
    
    this.showAlert_d = true;
    
    showAlert()
    //     this.alertType = 'error';
    //     this.alertMessage = 'vérifiez votre connexion';
    // Handle errors here
  }
},
    },
    mounted() {
      this.getData()
      setInterval(this.getData(), 5000);
      const toasts = document.getElementById('toasts');
 
    }
    
  }
</script>



<style lang="scss" scoped>

</style>