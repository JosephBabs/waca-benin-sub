<template>
    <div>
      <Nav />
      <PageHeader title="Documenetèque" />
      <Rapports />

      <Footer />
    </div>
  </template>
  
  <script>
  
    import Nav from "../components/Nav";
    import PageHeader from "../components/PageHeader";
    import Rapports from "../components/Rapports";
    import Footer from "../components/Footer";
    export default {
      components: {
        Footer,
        PageHeader,
        Rapports,
        Nav
      },
      head(){
        return {
          title: "WACA  | Gallery"
        }
      }
    }
  </script>
  