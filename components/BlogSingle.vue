<template>
  <section class="news_detail">
    <div class="container">
      <div class="row">
        <div class="col-xl-8 col-lg-7" v-for="actu in news" :key="actu.id">
          <div class="news_detail_left">
            <div class="news_detail_image_box">
              <img
                :src="
                  'https://waca.uigp.bj/web/public/storage/' + actu.cover
                "
                alt=""
              />
              <!-- <img :src="'https://waca.uigp.bj/web/public/storage/'+actu.cover" alt=""> -->
              <div class="news_detail_date_box">
                <p>{{ formatDate(actu.created_at) }}</p>
              </div>
            </div>
            <ul class="list-unstyled news_detail__meta">
              <li>
                <nuxt-link to="/news_detail"
                  ><i class="far fa-user-circle"></i>
                  {{ actu.author }}</nuxt-link
                >
              </li>
              <li>
                <nuxt-link to="/news_detail"
                  ><i class="far fa-comments"></i>
                  {{ actu.comments_count }}</nuxt-link
                >
              </li>
            </ul>
            <div class="news_detail_content">
              <h2>{{ actu.title }}</h2>
              <p class="news_detail_one_text">
                {{ actu.content }}
              </p>
            </div>
            <!-- <div class="news_detail__bottom">
              <p class="news_detail__tags">
                <span>Tags:</span>
                <a href="#">Agriculture,</a>
                <a href="#">Food,</a>
                <a href="#">Economy</a>
              </p>
              <div class="news_detail__social-list">
                <a href="#"><i class="fab fa-facebook-square"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-dribbble"></i></a>
              </div>
            </div> -->
            <!-- <div class="author-one">
              <div class="author-one__image">
                <img src="/assets/images/blog/author-1-1.jpg" alt="" />
              </div>
              
            </div> -->
            <comment />

            <div class="comment-form">
              <h3 class="comment-form__title">Leave a Comment</h3>
              <form action="#" class="comment-one__form">
                <div class="row">
                  <div class="col-xl-6">
                    <div class="comment_input_box">
                      <input type="text" placeholder="Full name" name="name" />
                    </div>
                  </div>
                  <div class="col-xl-6">
                    <div class="comment_input_box">
                      <input
                        type="text"
                        placeholder="Email address"
                        name="email"
                      />
                    </div>
                  </div>
                </div>
                <div class="row">
                  <div class="col-xl-12">
                    <div class="comment_input_box">
                      <textarea
                        name="message"
                        placeholder="Write message"
                      ></textarea>
                    </div>
                    <button type="submit" class="thm-btn comment-form__btn">
                      Submit Comment
                    </button>
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
        <div class="col-xl-4 col-lg-5">
          <div class="sidebar">
            <div class="sidebar__single sidebar__search">
              <form action="#" class="sidebar__search-form">
                <input type="search" placeholder="Search" />
                <button type="submit">
                  <i class="icon-magnifying-glass"></i>
                </button>
              </form>
            </div>
            <div class="sidebar__single sidebar__post">
              <h3 class="sidebar__title">Latest Posts</h3>
              <ul class="sidebar__post-list list-unstyled">
                <li>
                  <div class="sidebar__post-image">
                    <img src="/assets/images/blog/lp-1-1.jpg" alt="" />
                  </div>
                  <div class="sidebar__post-content">
                    <h3>
                      <a href="#" class="sidebar__post-content_meta"
                        ><i class="far fa-user-circle"></i> Admin</a
                      >
                      <nuxt-link to="/news_detail"
                        >Agriculture Miracle you Don't Know About</nuxt-link
                      >
                    </h3>
                  </div>
                </li>
                <li>
                  <div class="sidebar__post-image">
                    <img src="/assets/images/blog/lp-1-2.jpg" alt="" />
                  </div>
                  <div class="sidebar__post-content">
                    <h3>
                      <a href="#" class="sidebar__post-content_meta"
                        ><i class="far fa-user-circle"></i> Admin</a
                      >
                      <nuxt-link to="/news_detail"
                        >Agriculture Miracle you Don't Know About</nuxt-link
                      >
                    </h3>
                  </div>
                </li>
                <li>
                  <div class="sidebar__post-image">
                    <img src="assets/images/blog/lp-1-3.jpg" alt="" />
                  </div>
                  <div class="sidebar__post-content">
                    <h3>
                      <a href="#" class="sidebar__post-content_meta"
                        ><i class="far fa-user-circle"></i> Admin</a
                      >
                      <nuxt-link to="/news_detail"
                        >Agriculture Miracle you Don't Know About</nuxt-link
                      >
                    </h3>
                  </div>
                </li>
              </ul>
            </div>
            <div class="sidebar__single sidebar__category">
              <h3 class="sidebar__title">All Categories</h3>
              <ul class="sidebar__category-list list-unstyled">
                <li><a href="#">Agriculture</a></li>
                <li><a href="#">Organic Food</a></li>
                <li><a href="#">Dairy Farm</a></li>
                <li><a href="#">Economy Solution</a></li>
                <li><a href="#">Harvests Innovations</a></li>
              </ul>
            </div>
            <div class="sidebar__single sidebar__tags">
              <h3 class="sidebar__title">Popular Tags</h3>
              <div class="sidebar__tags-list">
                <a href="#">Agriculture,</a>
                <a href="#">Food,</a>
                <a href="#">Healthy,</a>
                <a href="#">Economy,</a>
                <a href="#">Organic,</a>
                <a href="#">Farm,</a>
                <a href="#">Dairy,</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Comment from "../components/comment";
export default {
  name: "BlogSingle",

  components: {
    Comment
  },
  data() {
    return {
      news: {}
    };
  },
  methods: {
    reloadPage() {
      location.reload(); // Reload the page
    },

    async getData() {
      const apiLink = dataT.apiUrl.link;

      const res = await fetch(
        "https://uigp.bj/api/wacaposts/" + this.$route.query.post
      );
      const finalRes = await res.json();
      // console.log(finalRes.post);
      const post = finalRes.post; // Assuming post is an object with properties

      this.news = post;
      if (this.$route.query.post !== this.news.id) {
        const post = await fetchData(this.$route.query.post);
        this.news = post;
      }
      // Display specific properties in the alert
      // alert("Post Title: " + post.title);
    },

    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    }
  },
  mounted() {
    this.getData();
    // Attach a click event listener to the <nuxt-link> element
    // const link = this.$el.querySelector('nuxt-link');
    // link.addEventListener('click', this.reloadPage); cma-B-nin-Web-main
  }
};
</script>

<style scoped></style>
