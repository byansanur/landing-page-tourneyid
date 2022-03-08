<template>
  <div>
    <v-row class="justify-center"> 
      <BgHero />
      <v-col cols="12" xs="12 d-flex align-content-start flex-wrap" sm="12 flex" md="12 flex" lg="12 d-flex" class="justify-space-between">
        
        <v-card class="justify-start mt-4" color="transparent" outlined tile>
          <v-card-title >
            <h1 style="color:black">
              Biggest Platform For <br/>
              Esport Tournament
            </h1>
            <br/>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptate placeat illum sequi esse tenetur voluptates dicta, magnam ad molestiae eos asperiores similique! In possimus corrupti doloremque necessitatibus? Quia, officia blanditiis.</p>
            <v-btn
              class="d-flex items-center flex-1 justify-center"
              color="#6D329D"
            >
              <v-text class="d-flex justify-space-around" style="color:white">Learn More</v-text>
            </v-btn> 
          </v-card-title>
        </v-card>
        <v-spacer/>
        <v-card class="d-flex justify-end ms-4">
          <v-img src="/bgheader-1.jpg" />
        </v-card>
      </v-col>

    </v-row>

    
    
    <!-- <v-container> -->
      <Feature/>
    <!-- </v-container> -->
  </div>
    
  
  
</template>

<script>
import BgHero from "../components/BgHero.vue";
import Feature from "./feature.vue";
export default {
    name: "IndexPage",
    components: { BgHero, Feature }
}
</script>
