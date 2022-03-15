<template>
  <div>
    <div>
      <v-row class="justify-space-between"> 
        <BgHero />
        <v-col cols="12" xs="12 d-flex align-content-start flex-wrap" sm="12 flex" md="12 flex" lg="12 d-flex mt-12" xl="12 flex-wrap mt-12" class="justify-space-between">
          
          <v-card class="d-flex justify-start mt-4"
          max-width="566" max-height="626" color="transparent" outlined tile>
            <v-card-title >
              <h1 style="color:black">
                Platform Turnamen Esport<br/>Terbesar Se-Indonesia
              </h1>
              <br/>
              <p style="color:white">Bentuk Tim Impian Anda Bersama kami dan Menangkan Setiap Turnamen</p>
              <br/>
              <v-btn
                class="d-flex items-center flex-1 justify-center"
                color="#6D329D"
              >
                <v-text class="d-flex justify-space-around" style="color:white">Selengkapnya</v-text>
              </v-btn> 
            </v-card-title>
          </v-card>
          
          <v-card class="d-flex justify-end ms-4" height="345" width="566" lg="4">
            <v-img src="/bgheader-1.jpg" />
          </v-card>
        </v-col>

      </v-row>

    </div>
    <div>
      <Feature class="mt-24"/>
    </div>
  </div>
    
  
  
</template>

<script>
import BgHero from "../components/BgHero.vue";
import Feature from "./feature.vue";
export default {
    name: "IndexPage",
    components: { BgHero, Feature },
    data () {
      return {
        selectedItem: 1,
        itemCarousel: [
          {
            title: "Title Carousel 1",
            subTitle: "sub title"
          },
          {
            title: "Title Carousel 2",
            subTitle: "sub title"
          },
          {
            title: "Title Carousel 3",
            subTitle: "sub title"
          }
        ]
      }
    }
}
</script>

<style scoped>
.titleHeader {
  font-weight: 700;
  font-size: 150%;
  justify-content: center!important;
  align-items: center!important;
  text-align: center!important;
}
.titleSubHeader {
  font-weight: 400;
  font-size: 130%;
  justify-content: center!important;
  align-items: center!important;
  text-align: center!important;
}
</style>
