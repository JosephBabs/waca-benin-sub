<template>
  <section class="blog-one news">
    <div class="container">
      <div class="row">
        <div class="col-xl-4 col-lg-4" v-for="actu in news" :key="actu.id">
          <div class="blog_one_single mb-30">
            <div class="blog_one_image">
              <div class="blog_image">
                <img
                :src="
                  'https://waca.uigp.bj/web/public/storage/' + actu.cover
                "
                  alt="Blog One Image"
                />
                <div class="blog_one_date_box">
                  <p>{{formatDate(actu.created_at)}}</p>
                </div>
              </div>
              <div class="blog-one__content">
                <ul class="list-unstyled blog-one__meta">
                  <li>
                    <nuxt-link :to="'/actus_detail?post='+actu.id"
                      ><i class="far fa-user-circle"></i> {{actu.author}}</nuxt-link
                    >
                  </li>
                  <li>
                    <nuxt-link :to="'/actus_detail?post='+actu.id"
                      ><i class="far fa-comments"></i> {{ actu.comments_count }}</nuxt-link
                    >
                  </li>
                </ul>
                <h3>
                  <nuxt-link :to="'/actus_detail?post='+actu.id"
                    >{{actu.title}}</nuxt-link
                  >
                </h3>
                <div class="blog_one_text">
                  <p>
                    {{actu.content.substring(0, 100)}}
                  </p>
                </div>
                <div class="read_more_btn">
                  <nuxt-link :to="'/actus_detail?post='+actu.id"
                    ><i class="fa fa-angle-right"></i>Lire Plus</nuxt-link
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Actualités",

  data() {
    return {
      news: []
    };
  },
  methods: {
    async getData() {
      // const apiLink = data.apiUrl.link;
      // apiLink+
      const res = await fetch("https://uigp.bj/api/wacaposts");
      const finalRes = await res.json();
      this.news = finalRes.posts;
    },
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    }
  },
  mounted() {
    this.getData();
  },
  computed: {
    // truncatedDescription( content) {
    //   if (content) {
    //     // Truncate the description to the first 100 characters
    //     return content.toString.substring(0, 100);
    //   }
    //   // If the description is empty, you can provide a default value or handle it accordingly
    //   return "No description available";
    // }
  }
};
</script>

<style scoped></style>
