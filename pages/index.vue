<template>
  <div>
    <v-row class="justify-space-between"> 
      <BgHero />
      <v-col cols="12" xs="12 d-flex align-content-start flex-wrap" sm="12 flex" md="12 flex" lg="12 d-flex" xl="12 flex-wrap" class="justify-space-between">
        
        <v-card class="d-flex justify-start mt-4"
        max-width="566" color="transparent" outlined tile>
          <v-card-title >
            <h1 style="color:black">
              Biggest Platform For
              Esport Tournament
            </h1>
            <br/>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
            <br/>
            <v-btn
              class="d-flex items-center flex-1 justify-center"
              color="#6D329D"
            >
              <v-text class="d-flex justify-space-around" style="color:white">Learn More</v-text>
            </v-btn> 
          </v-card-title>
        </v-card>
        
        <v-spacer/>

        <v-card class="d-flex justify-end ms-4" height="261" width="566" lg="4">
          <v-img src="/bgheader-1.jpg" />
        </v-card>
      </v-col>

    </v-row>

    <v-row class="justify-space-around">
      <v-col cols="12" xs="12 d-flex align-content-start flex-wrap" sm="12 flex" md="12 flex" lg="12 flex" class="justify-space-around">

        <v-list  color="transparent" v-model="selectedItem" >
            <v-list-item-group class="d-flex justify-space-around mt-2"  >
              <v-list-item
                v-for="(item, i) in itemCarousel"
                :key="i"
                :to="item.to"
                router
              >
                <v-list-item-content >
                  <v-list-item-title  v-text="item.title" style="color: white;" class="titleHeader"/>
                  <v-list-item-subtitle v-text="item.subTitle" style="color: gray" class="titleSubHeader"/>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>

      </v-col>

    </v-row>

    <Feature class="mt-24"/>
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
