<template>
  <section class="gallery_two">
    <div class="container">
      <div
        class="row masonary-layout"
        style="position: relative; height: 1011px;"
      >
        <div v-for="item in gallery"
              :key="item.id"
          class="col-xl-4 col-lg-6 col-md-6 masonary-item"
          
        >
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img :src="item.image" 
                :alt="item.title" />
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a
                    class="img-popup"
                    :href="item.image"
                    ><span class="icon-plus-symbol"></span
                  ></a>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- <div class="col-xl-4 col-lg-6 col-md-6 masonary-item" style="position: absolute; left: 400px; top: 0px;">
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img src="/assets/images/gallery/gallery-2-img-2.jpg" alt="">
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a class="img-popup" href="/assets/images/gallery/gallery-2-img-2.jpg"><span class="icon-plus-symbol"></span></a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-4 col-lg-6 col-md-6 masonary-item" style="position: absolute; left: 800px; top: 0px;">
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img src="/assets/images/gallery/gallery-2-img-3.jpg" alt="">
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a class="img-popup" href="/assets/images/gallery/gallery-2-img-3.jpg"><span class="icon-plus-symbol"></span></a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-4 col-lg-6 col-md-6 masonary-item" style="position: absolute; left: 0px; top: 280px;">
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img src="/assets/images/gallery/gallery-2-img-4.jpg" alt="">
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a class="img-popup" href="/assets/images/gallery/gallery-2-img-4.jpg"><span class="icon-plus-symbol"></span></a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-4 col-lg-6 col-md-6 masonary-item" style="position: absolute; left: 800px; top: 280px;">
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img src="/assets/images/gallery/gallery-2-img-5.jpg" alt="">
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a class="img-popup" href="/assets/images/gallery/gallery-2-img-5.jpg"><span class="icon-plus-symbol"></span></a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-4 col-lg-6 col-md-6 masonary-item" style="position: absolute; left: 0px; top: 731px;">
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img src="/assets/images/gallery/gallery-2-img-6.jpg" alt="">
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a class="img-popup" href="/assets/images/gallery/gallery-2-img-6.jpg"><span class="icon-plus-symbol"></span></a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-4 col-lg-6 col-md-6 masonary-item" style="position: absolute; left: 400px; top: 731px;">
          <div class="gallery_two_single">
            <div class="gallery_two_image">
              <img src="/assets/images/gallery/gallery-2-img-7.jpg" alt="">
              <div class="gallery_two_hover_box">
                <div class="gallery_two_icon">
                  <a class="img-popup" href="/assets/images/gallery/gallery-2-img-7.jpg"><span class="icon-plus-symbol"></span></a>
                </div>
              </div>
            </div>
          </div>
        </div> -->
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Gallery",
  data() {
    return {
      gallery: [],
      galleryV: [],
      currentIndex: null,
      lightboxVisible: false
    };
  },
  methods: {
    async getData() {
      // const mediaLink = data.postImg.link;
      // const apiLink = data.apiUrl.link;
      const res = await fetch("https://uigp.bj/api/galleries");
      const finalRes = await res.json();
      this.gallery = finalRes.galleries;
    },
    async getData1() {
      // const mediaLink = data.postImg.link;
      // const apiLink = data.apiUrl.link;
      const res1 = await fetch( "https://uigp.bj/api/video-galleries");
      const finalRes1 = await res1.json();
      this.galleryV = finalRes1.galleries;
    },
    
    
    
  },
  mounted() {
    this.getData();
    this.getData1();
    
    new GLightbox({
      selector: ".img-popup"
    });
  }
};
</script>

<style scoped></style>
