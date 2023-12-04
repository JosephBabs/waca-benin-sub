<template>
    <section class="bx-testimonial" id="financement">
      <div
        class="bx-testimonial_bg"
        style="background-image: url(/assets/images/testimonials/bx-testi-bg.png)"
      ></div>
      <div class="container">
        <div class="block-title text-center">
          <p>Le Projet WACA au BENIN</p>
          <h3>Financement</h3>
          <div class="leaf">
            <img src="/assets/images/resources/leaf.png" alt="" />
          </div>
        </div>
        <div class="row">
          <div class="col-xl-12">
            <table class="cart_table_box cart_table" border="1">
              <thead>
                
                <tr style="font-weight: 800; text-align: start;">
                  <td style="background-color: #f3eea6; padding: 1em;">SN.</td>
                  <td style="background-color: #f3eea6; padding: 1em;" colspan="3" >Libelé</td>
                  <td style="padding: 1em;">Descrtiption</td>
                </tr>
              </thead>
              <thead>
              <tr v-for="el in indics" :key="el.id" style="font-weight: 400; text-align: start;">
                <td style="font-weight: 800; text-align: center; padding: 5px; background-color: #f3eea6;">{{ el.id }}</td>
                <td style="font-weight: 800; text-align: start; padding: 5px; background-color: #f3eea6;">{{ el.titre }}</td>
                <td colspan="3">{{ el.description }}</td>
              </tr></thead>
            </table>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: "Financement",
    data() {
      return {
        indics: [
       
          {
            id: "1",
            titre: "Titre du Projet",
            description: "PROJET D’INVESTISSEMENT DE RESILIENCE WACA-BENIN",
            
          },
          {
            id: "2",
            titre: "Référence",
            description: "P 162337",
            
          },
          {
            id: "3",
            titre: "Agence d’exécution",
            description: "MINISTERE DU CADRE DE VIE ET DU DEVELOPPEMENT DURABLE",
            
          },
          {
            id: "4",
            titre: "Accords de financement",
            description: "FINANCEMENT BANQUE MONDIALE, GEF, NDF et GVT-B",
            
          },
          {
            id: "5",
            titre: "Montant Global",
            description: "87 168 708 dont 24 000 000 $ USD de fonds additionnel",
            
          },
          {
            id: "6",
            titre: "Date de signature",
            description: "21-avril -2018",
            
          },
          {
            id: "7",
            titre: "Date de mise en vigueur",
            description: "17-août -2018",
            
          },
          {
            id: "8",
            titre: "Durée effective d’exécution",
            description: "5 ans",
            
          },
          {
            id: "9",
            titre: "Date d’achèvement effective",
            description: "31 décembre 2023",
            
          },
          {
            id: "10",
            titre: "Objectif de développement du Projet",
            description: "Renforcer la résilience des communautés et des zones cibles dans la zone côtière ouest africaine",
            
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped></style>
  