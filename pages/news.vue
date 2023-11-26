<template>
  <div>
    <Nav />
    <PageHeader title="News" />
    <actus />
    <Footer />
  </div>
</template>

<script>

  import Nav from "../components/Nav";
  import PageHeader from "../components/PageHeader";
  import Footer from "../components/Footer";
  import actus from "../components/actus";
  export default {
    components: {
      actus,
      Footer,
      PageHeader,
      Nav
    },
    head(){
      return {
        title: "WACA  | News"
      }
    }
  }
</script>
