<template>
  <section class="service_one" id="composanteProjet">
    <div class="container">
      <div class="block-title text-center">
        <p></p>
        <h3>Composantes du Projet</h3>
        <div class="leaf">
          <img src="/assets/images/resources/leaf.png" alt="" />
        </div>
      </div>
      <div class="row">
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp">
            <div class="content">
              <h5>Intégration régionale</h5>
              <p>
                L’objectif de cette composante est le renforcement de
                l’intégration régionale en Afrique de l’Ouest pour
                l’amélioration de la gestion des zones côtières.
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-1.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp" data-wow-delay="300ms">
            <div class="content">
              <h5>Renforcement des politiques et <br />institutions
nationales</h5>
              <p>
                Cette seconde composante va permettre
d’accompagner le Bénin pour fixer son cadre politique,
stratégique, règlementaire et institutionnel pour le
suivi et la gestion de ses espaces littoraux
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-2.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp" data-wow-delay="600ms">
            <div class="content">
              <h5>Renforcement des investissements <br />nationaux physiques et sociaux</h5>
              <p>
                Les résultats de l’évaluation du risque multi-aléa réalisée au Bénin dans le cadre de la préparation du projet
WACA (IMDC, 2017) ont confirmé les secteurs d’interventions prioritaires, l
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-3.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
        <div class="col-xl-3 col-lg-3 col-md-6">
          <div class="service_1_single wow fadeInUp" data-wow-delay="900ms">
            <div class="content">
              <h4>Coordination nationale</h4>
              <p>
                Mettre en place un cadre institutionnel approprié
et opérationnel pour une gestion efficace du projet
WACA.
              </p>
            </div>
            <div class="service_1_img">
              <!-- <img
                src="/assets/images/service/service-1-img-4.jpg"
                alt="Service Image"
              /> -->
              <div class="hover_box">
                <nuxt-link to="/service-detail"
                  ><span class="icon-left-arrow"></span
                ></nuxt-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ServiceOne"
};
</script>

<style scoped></style>
