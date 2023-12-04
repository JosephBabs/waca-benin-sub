<template>
  <section class="bx-testimonial" id="indicateursDeResultats">
    <div
      class="bx-testimonial_bg"
      style="background-image: url(/assets/images/testimonials/bx-testi-bg.png)"
    ></div>
    <div class="container">
      <div class="block-title text-center">
        <p>Le Projet WACA au BENIN</p>
        <h3>INDICATEURS DE RESULTATS</h3>
        <div class="leaf">
          <img src="/assets/images/resources/leaf.png" alt="" />
        </div>
      </div>
      <div class="row">
        <div class="col-xl-12">
          <table class="cart_table_box cart_table" border="1">
            <thead>
              
              <tr style="font-weight: 800; text-align: center;">
                <td style="padding: 1em;">SN.</td>
                <td colspan="3" style="padding: 1em;">Description</td>
                <td style="padding: 1em; background-color: #f3eea6;">Indcateur</td>
              </tr>
            </thead>
            <thead>
            <tr v-for="el in indics" :key="el.id" style="font-weight: 400; text-align: center;">
              <td>{{ el.id }}</td>
              <td colspan="3">{{ el.description }}</td>
              <td style="padding: 5px; background-color: #f3eea6;">{{ el.indicateur }}</td>
            </tr></thead>
          </table>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TestimonialFour",
  data() {
    return {
      indics: [
        {
          id: "1",
          titre: "Indicateur 1",
          description: "Nombre de ménages des zones côtières ciblées moins exposés au risque d'érosion",
          indicateur: "4.790"
        },
        {
          id: "2",
          titre: "Indicateur 1",
          description: "Nombre de ménages des zones côtières ciblées moins exposés au risque d'inondation",
          indicateur: "4.790"
        },
        {
          id: "2.1",
          titre: "Indicateurs clés intermédiaires :",
          description: "Score sur les instruments de politique et cadre juridique (0-5)",
          indicateur: "2"
        },
        {
          id: "2.3",
          titre: "",
          description: "Nombre de plans d’aménagement et de gestion de la réserve de Biosphère et Aires Communautaires de Conservation de la Biodiversité élaborés / actualisés dans la zone du projet",
          indicateur: "2"
        },
        {
          id: "3.1",
          titre: "",
          description: "Superficie de la zone côtière ciblée avec des mesures de lutte contre les inondations",
          indicateur: "5.200"
        },
        {
          id: "3.4",
          titre: "",
          description: "Nombre d’écosystèmes naturels conservés et/ou restaurés",
          indicateur: "1"
        },
        {
          id: "3.5",
          titre: "",
          description: "Nombre de ménages affectés des communautés côtières ayant bénéficié du financement des AaGRs ou de projets sociaux ",
          indicateur: "424"
        },
        {
          id: "3.6",
          titre: "",
          description: "Nombre de plans d’aménagement et de gestion de la réserve de Biosphère et Aires Communautaires de Conservation de la Biodiversité mis en œuvre dans la zone du projet",
          indicateur: "4"
        },
        {
          id: "3.7",
          titre: "",
          description: "Nombre d’Activités alternatives Génératrices de Revenus financés dans la zone du projet",
          indicateur: "207"
        },
        {
          id: "3.7a",
          titre: "",
          description: "Pourcentage de femmes bénéficiaires des Activités alternatives Génératrices de Revenus financés dans la zone du projet",
          indicateur: "80%"
        },
        {
          id: "4",
          titre: "",
          description: "Pourcentage des bénéficiaires (individu) ciblés avec une note « Satisfait » ou plus, au sujet des interventions du projet",
          indicateur: "55%"
        }
      ]
    };
  }
};
</script>

<style scoped></style>
