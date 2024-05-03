<template>
  <div>
    <footer class="site-footer">
      <div class="site-footer_farm_image">
        <img
          src="/assets/images/resources/site-footer-farm.png"
          alt="Farm Image"
        />
      </div>

      <div class="container">
        <div class="row no-gutters">
          <div class="col-xl-4 col-lg-4 col-md-6">
            <div
              class="footer-widget__column footer-widget__about wow fadeInUp"
              data-wow-delay="100ms"
            >
              <div class="footer-widget__title">
                <h3>A propos</h3>
              </div>
              <div class="footer-widget_about_text">
                <p>
                  Le Programme de gestion du littoral ouest-africain (WACA) a
                  été initié pour apporter une réponse régionale aux populations
                  d’Afrique de l’Ouest vivant sur le littoral en raison de leur
                  vulnérabilité face aux effets physiques, écologiques et
                  anthropiques du changement climatique
                </p>
              </div>
              
            </div>
          </div>
          <div class="col-xl-2 col-lg-2 col-md-6">
            <div
              class="footer-widget__column footer-widget__link wow fadeInUp"
              data-wow-delay="200ms"
            >
              <div class="footer-widget__title">
                <h3>Liens:</h3>
              </div>
              <ul class="footer-widget__links-list list-unstyled">
                <li><a href="/apropos">A propos</a></li>
                <li><a href="/gallery">Galerie</a></li>
              </ul>
            </div>
          </div>
          <div class="col-xl-3 col-lg-3 col-md-6">
            
          </div>
          <div class="col-xl-3 col-lg-3 col-md-6">
            <div
              class="footer-widget__column footer-widget__contact wow fadeInUp"
              data-wow-delay="400ms"
            >
              <div class="footer-widget__title">
                <h3>Contacts</h3>
              </div>
              <div class="footer-widget_contact">
                <p>Complexe CEN-SAD LAICO, <br />Villa n°8 rue Steeve BIKO
01 BP 3502 Cotonou </p>
                <a href="mailto:uigpwaca.infos@gouv.bj"
                  >uigpwaca.infos@gouv.bj</a
                ><br />
                <a href="tel:+22999990608"> (+229) 99 99 06 08</a>
                <div class="site-footer__social">
                  <a href="#"><i class="fab fa-facebook-square"></i></a>
                  <a href="#"><i class="fab fa-twitter"></i></a>
                  <a href="#"><i class="fab fa-instagram"></i></a>
                  <a href="#"><i class="fab fa-dribbble"></i></a>
                </div>
              </div>

              
            </div>
          </div>

          <form  @submit.prevent="submitDat">
                  
                  <div class="footer-widget__title">
                    <br>
                    <br>
                <h3>Inscrivez-vous à notre newsletter</h3>
              </div>
              
                <div class="footer_input-box">
                  <input type="email"
                    placeholder="E-mail"
                    name="email"
                    />
                  <button type="submit" class="button"> 
                    <i class="fa fa-check"></i>
                  </button>
                </div>
              </form>
              
        </div>
      </div>
    </footer>

    <div class="site-footer_bottom">
      <div class="container">
        <div class="site-footer_bottom_copyright">
          <p>&copy; Copyright {{ new Date().getFullYear() }} | <a href="#"></a> | +229 94 44 41 44</p>
                </div>
        <div class="site-footer_bottom_menu">
          <!-- <ul class="list-unstyled">
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Terms of Use</a></li>
          </ul> -->
        </div>
      </div>
    </div>

    <a
      @click="scrollTop"
      href="#"
      class="scroll-to-target scroll-to-top"
      :style="`display: ${scrollBtn ? 'block' : 'none'}`"
      ><i class="fa fa-angle-up"></i
    ></a>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      scrollBtn: false
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },

  methods: {
    handleScroll() {
      if (window.scrollY > 70) {
        this.scrollBtn = true;
      } else if (window.scrollY < 70) {
        this.scrollBtn = false;
      }
    },

    scrollTop() {
      window.scrollTo(0, 0);
    }
  }
};
</script>

<style scoped></style>
