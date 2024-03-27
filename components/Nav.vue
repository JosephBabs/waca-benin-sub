<template>
  <div class="site-header__header-one-wrap">
    <div class="topbar-one">
      <div
        class="topbar_bg"
        style=""
      ></div>
      <div class="container">
        <div class="topbar-one__left">
          <a href="mailto:needhelp@tripo.com"
            ><span class="icon-message"></span>uigpwaca.infos@gouv.bj</a
          >
          <!-- <a href="tel:+22999990608"
            ><span class="icon-phone-call"></span>(+229)99 99 06 08</a
          > -->
        </div>
        <div class="topbar-one__middle">
          <a href="/" class="main-nav__logo">
            <img
              src="/assets/images/resources/logo.png"
              class="main-logo"
              alt="Awesome Image" style="height: auto; width: 10em;"
            />
          </a>

          <a href="/" class="main-nav__logo">
            <img
              src="/assets/images/logo-bm.png"
              class="main-logo"
              alt="Awesome Image" style="height: auto; width: 20em;"
            />
          </a>
        </div>
        <div class="topbar-one__right">
          <div class="topbar-one__social">
            <a href="#"><i class="fab fa-facebook-square"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-dribbble"></i></a>
          </div>
        </div>
      </div>
    </div>

    <header class="main-nav__header-one">
      <nav
        :class="`header-navigation stricky clearfix ${
          sticky ? 'stricked-menu stricky-fixed' : ''
        }`"
      >
        <div class="container clearfix">
          <!-- Brand and toggle get grouped for better mobile display -->
          <div class="main-nav__left">
            <a
              href="#"
              class="main-nav__search search-popup__toggler"
              @click="searchPopupStatusChange"
              ><i class="icon-magnifying-glass"></i
            ></a>
            <a href="#" class="side-menu__toggler">
              <i @click="mobileToggle = !mobileToggle" class="fa fa-bars"></i>
            </a>
          </div>
          <div class="main-nav__main-navigation">
            <ul class="main-nav__navigation-box">
              <li class="dropdown current">
                <nuxt-link to="/">Acceuil</nuxt-link>
                <!-- /.sub-menu -->
              </li>
              <li class="dropdown">
                <nuxt-link to="/apropos">A propos</nuxt-link>
                <ul> 
                  <li><nuxt-link to="/apropos#wacaRegional">Programme WACA Régional</nuxt-link></li>
                  <li> 
                    <nuxt-link to="/apropos#wacaBenin">Programme WACA Bénin</nuxt-link>
                  </li> 
                </ul>
              </li>
              <li class="dropdown">
                <nuxt-link to="/actus">Actualités</nuxt-link>
                <!-- /.sub-menu -->
              </li>
              <li class="dropdown">
                <nuxt-link to="/#financement">Financement</nuxt-link>
                <!-- /.sub-menu -->
              </li>
              <li class="dropdown">
                <nuxt-link to="/#composanteProjet">Composantes du Projet</nuxt-link>
                <!-- /.sub-menu -->
              </li>
              <li class="dropdown">
                <nuxt-link to="#">Plus +</nuxt-link>
                <ul>
                  <li>
                    <nuxt-link to="#calendrierEtCartographie">Calendrier et Cartographie d'Intervention</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="#indicateursDeResultats">Indicateurs de Résultats</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/gallery">Galerie</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="#partenaires">Ressources</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="#partenaires">Partenaires</nuxt-link>
                  </li>
                </ul>
                <!-- /.sub-menu -->
              </li>
              
              
              
              <!-- <li>
                <nuxt-link to="/contact">Contact</nuxt-link>
              </li> -->
            </ul>
          </div>
          <!-- /.navbar-collapse -->

          
        </div>
      </nav>

      <nav
        class="mobile-nav__container"
        :style="`display: ${mobileToggle ? 'block' : 'none'}`"
      >
        <!-- content is loading via js -->

        <ul class="main-nav__navigation-box">
          <li class="dropdown current">
            <div class="menu-holder">
              <li class="dropdown current">
                <nuxt-link to="/">Acceuil</nuxt-link>
                <!-- /.sub-menu -->
              </li>
            </div>
            
            <!-- /.sub-menu -->
          </li>
          <li class="dropdown">
            <div class="menu-holder">
              <nuxt-link to="/apropos">A propos</nuxt-link><button class="dropdown-btn">
                <i class="fa fa-angle-right"></i>
              </button>
            </div>
            <ul>
              <li><nuxt-link to="/apropos#wacaRegional">Programme WACA Régional</nuxt-link></li>
                  <li> 
                    <nuxt-link to="/apropos#wacaBenin">Programme WACA Bénin</nuxt-link>
                  </li> 
            </ul>
            <!-- /.sub-menu -->
          </li>
          <li class="dropdown">
            <div class="menu-holder">
              <nuxt-link to="/news">Actualités</nuxt-link>
            </div>
            <!-- /.sub-menu -->
          </li>
          <li class="dropdown">
            <div class="menu-holder">
              <nuxt-link to="/#financement">Financement</nuxt-link>
               </div>
            <!-- /.sub-menu -->
          </li>
          <li class="dropdown">
            <div class="menu-holder">
              <nuxt-link to="/#composanteProjet">Composantes du Projet</nuxt-link>
             </div>
            <!-- /.sub-menu -->
          </li>

          <li class="dropdown">
            <div class="menu-holder">
              Plus +<button class="dropdown-btn">
                <i class="fa fa-angle-right"></i>
              </button>
            </div>
            <ul>
                  <li>
                    <nuxt-link to="/#calendrierEtCartographie">Calendrier et Cartographie d'Intervention</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/#indicateursDeResultats">Indicateurs de Résultats</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/gallery">Galerie</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/#partenaires">Ressources</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/#partenaires">Partenaires</nuxt-link>
                  </li>
                </ul>
            <!-- /.sub-menu -->
          </li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
import { mapMutations } from "vuex";

export default {
  name: "Nav",
  data() {
    return {
      sticky: false,
      mobileToggle: false,
    };
  },
  computed: {
    searchPopup() {
      return this.$store.state.searchPopupStatus;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 70) {
        this.sticky = true;
      } else if (window.scrollY < 70) {
        this.sticky = false;
      }
    },
    ...mapMutations({
      searchPopupStatusChange: "changeSearchPopupStatus",
    }),
  },
};
</script>

<style scoped></style>
