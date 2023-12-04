<template>
  <div>
    <Nav />
    <PageHeader title="Actualités" />
    <BlogSingle />
    <Footer />
  </div>
</template>

<script>

  import Nav from "../components/Nav";
  import PageHeader from "../components/PageHeader";
  import Footer from "../components/Footer";
  import BlogSingle from "../components/BlogSingle";
  export default {
    components: {
      BlogSingle,
      Footer,
      PageHeader,
      Nav
    },
    head(){
      return {
        title: "WACA  | Actualités"
      }
    }
  }
</script>
