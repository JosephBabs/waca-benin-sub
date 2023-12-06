<template>

  <section class="page-header" style="background-image: url(/assets/images/backgrounds/page-header-contact.jpg); 
background-color: rgba(0, 255, 0, 0.2);">
    <div class="container">
      <h2>{{ title }}</h2>
      <ul class="thm-breadcrumb list-unstyled">
        <li><nuxt-link to="/">Accueil</nuxt-link></li>
        <li><span>{{ title }}</span></li>
      </ul>
    </div>
  </section>

</template>

<script>
  export default {
    name: "PageHeader",
    props: {
      title: {
        type: String
      }
    }

  }
</script>

<style scoped>

</style>
