<template>
  <div>
    <Nav />
    <Slider />
    <AboutOne />
    <ServiceOne />
    <FeaturedOne />
    <Cal />
    <BlogOne />
    <Footer />
  </div>
</template>

<script>
import Slider from "../components/Slider";
import Nav from "../components/Nav";
import AboutOne from "../components/AboutOne";
import ServiceOne from "../components/ServiceOne";
import BrandOne from "../components/BrandOne";
import FeaturedOne from "../components/FeaturedOne";
import Cal from "../components/cal";
import VideoOne from "../components/VideoOne";
import TestimonialOne from "../components/TestimonialOne";
import RecentProject from "../components/RecentProject";
import Benefits from "../components/Benefits";
import ProductOne from "../components/ProductOne";
import BlogOne from "../components/BlogOne";
import CallToActionOne from "../components/CallToActionOne";
import Footer from "../components/Footer";
export default {
  components: {
    Footer,
    CallToActionOne,
    BlogOne,
    ProductOne,
    Benefits,
    RecentProject,
    TestimonialOne,
    VideoOne,
    FeaturedOne,
    Cal,
    BrandOne,
    ServiceOne,
    AboutOne,
    Slider,
    Nav,
  },
};
</script>
