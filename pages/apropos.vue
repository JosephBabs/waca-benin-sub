<template>
  <div>
    <Nav />
    <PageHeader title="A propos" />
    <AboutOne />
    <AboutTwo />
    <financement /> 
    <TestimonialFour />
    <!-- <BrandOne /> -->
    <Footer />
  </div>
</template>

<script>

  import Nav from "../components/Nav";
  import PageHeader from "../components/PageHeader";
  import Footer from "../components/Footer";
  import AboutOne from "../components/AboutOne";
  import AboutTwo from "../components/AboutTwo";
  import Financement from "../components/financement";
  import TestimonialFour from "../components/TestimonialFour";
  import BrandOne from "../components/BrandOne";
  import VideoOne from "../components/VideoOne";
  import ProductOne from "../components/ProductOne";
  import TeamOne from "../components/TeamOne";
  import CallToActionOne from "../components/CallToActionOne";
  export default {
    components: {
      CallToActionOne,
      TeamOne,
      ProductOne,
      VideoOne,
      BrandOne,
      TestimonialFour,
      AboutTwo,
      Financement,
      AboutOne,
      Footer,
      PageHeader,
      Nav
    },
    head(){
      return {
        title: "WACA  | A propos"
      }
    }
  }
</script>
