<template>
  <section class="banner-section banner-one">

    <div class="banner-carousel">
      <!-- Slide Item -->
      <no-ssr>
      <carousel :items="1" :autoplay="true" :nav="false">

        <div class="slide-item">
          <div class="image-layer" style="background-image: url(/assets/images/main-slider/slide_v1_1.jpg);">
          </div>
          <div class="auto-container">
            <div class="content-box">
              <div class="content">
                <div class="inner">
                  <div class="sub-title">(WACA-Régional)</div>
                  <h2>Le Programme de gestion du<br> littoral Ouest-Africain</h2>
                  <div class="link-box">
                    <nuxt-link to="/apropos" class="thm-btn">En Savoir Plus</nuxt-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- Slide Item -->
        <div class="slide-item">
          <div class="image-layer" style="background-image: url(/assets/images/main-slider/slide_v1_2.jpg);">
          </div>
          <div class="auto-container">
            <div class="content-box">
              <div class="content">
                <div class="inner">
                  <div class="sub-title">(WACA-Régional)</div>
                  <h2>Le Projet WACA<br> au Bénin</h2>
                  <div class="link-box">
                    <nuxt-link to="/apropos" class="thm-btn">En Savoir Plus</nuxt-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- Slide Item -->
        <div class="slide-item">
          <div class="image-layer" style="background-image: url(/assets/images/main-slider/slide_v1_3.jpg);">
          </div>
          <div class="auto-container">
            <div class="content-box">
              <div class="content">
                <div class="inner">
                  <div class="sub-title">Le Projet WACA</div>
                  <h2>PROJET D’INVESTISSEMENT DE <br>RESILIENCE WACA-BENIN</h2>
                  <div class="link-box">
                    <nuxt-link to="/apropos" class="thm-btn">En Savoir Plus</nuxt-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </carousel>
      </no-ssr>
    </div>
  </section>
</template>

<script>

    export default {
      name: "Slider",
      data(){
          return {

          }
      }
    }
</script>

<style scoped>

</style>
