<template>
    <section class="pricing-one pricing-page " id="rapports">
          <div class="container">
            <br>
              <div class="block-title text-center">
                  <h1 class="block-title__title">Rapports</h1><!-- /.block-title__title -->
              </div><!-- /.block-title -->
            
          
              <div class="card-row">
                  <div class="card" v-for="file in files" :key="file.id">
                  <h2>{{ file.title }}</h2>
                  <button @click="downloadFile(file.url)">Télécharger</button>
                  </div>
              </div>
        
      </div>
          <!-- /.container -->
      </section>
  </template>
  
  <script>
      export default {
          name: "Rapports",
          data() {
      return {
        files: [
          { id: 1, title: 'revisé_Clean_PAR-Curage_chenal_Gbaga_BENIN_V02-01-2024_RSA_Review-DD-12-03-2024', url: 'https://pfc.uigp.bj/assets/pdf/Rapport_revisé_Clean_PAR-Curage_chenal_Gbaga_BENIN_V02-01-2024_RSA_Review-DD-12-03-2024.pdf' },
          { id: 2, title: '240312 PGES DE EIES CURAGE MECANIQUE GBAGA _BENIN_070324_Suivi Mod._approuvé', url: 'https://pfc.uigp.bj/assets/pdf/240312 PGES DE EIES CURAGE MECANIQUE GBAGA _BENIN_070324_Suivi Mod_approuve.pdf' },
          { id: 3, title: 'ANNEXE~PAR Bénin-06-03-2024 -approved-25-03-2024', url: 'https://pfc.uigp.bj/assets/pdf/ANNEXE~PAR Bénin-06-03-2024 -approved-25-03-2024.pdf' },
          { id: 4, title: '240312 EIES CURAGE MECANIQUE GBAGA _VERSION UNIQUE BENIN-TOGO (1)_clean', url: 'https://pfc.uigp.bj/assets/pdf/240312 EIES CURAGE MECANIQUE GBAGA _VERSION UNIQUE BENIN-TOGO (1)_clean.pdf' }
        ]
      };
    },
    methods: {
      downloadFile(url) {
        const link = document.createElement('a');
        link.href = url;
        link.download = true;
        link.click();
      }
    }
      }
  </script>

  <style scoped>
  .card-row {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: space-between;
    padding: 20px;
  }
  
  .card {
    flex: 1 1 calc(25% - 20px);
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 20px;
    gap: 20px;
    justify-content: space-between;
    text-align: center;
    width: 20%;
    background-color: #f9f9f9;
  }
  
  .card h2 {
    font-size: 1.2rem;
    margin-bottom: 10px;
    color: #333;
  }
  
  .card button {
    background-color: #00a2b4;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .card button:hover {
    background-color: #0056b3;
  }
  
  @media (max-width: 768px) {
    .card {
      flex: 1 1 calc(100% - 20px); /* 1 card per row on mobile */
    }
  }
  </style>
  