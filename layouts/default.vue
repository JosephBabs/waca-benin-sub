<template>
  <div class="page-wrapper">
    <nuxt />
    <SearchPopup />
    
  </div>
</template>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<style scoped>
    .client-message{
        background: red;
        color: #fff;
        font-family: Poppins;
        font-weight: Bold;
        font-size: 8vw;
        display: none;
        position: fixed;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        padding: 5%;
    }
    .client-message p{
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        line-height: 1.3;
    }
</style>
<script>
import SearchPopup from "../components/SearchPopup";
export default {
  components: {
    SearchPopup,
  },
  head() {
    return {
      title: "WACA - Vue Nuxt Template for Agriculture Farm & Farmers",
    };
  },
  mounted() {

    this.$nextTick(() => {
      this.$nuxt.$loading.start();
      setTimeout(() => this.$nuxt.$loading.finish(), 500);
    });
  },
};
</script>

<style></style>
