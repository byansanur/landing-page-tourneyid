<template>
  <v-app>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      elevate-on-scroll
      absolute
      outlined
      color="#FFA45E"
      light
    >
    <v-row class="justify-space-between">
      <v-col  class="columnHeader col-10 d-flex">
      
        <a href="/">
        <v-img class="flex items-center flex-1 justify-center lg:justify-start mt-2 ms-2">
          <TourneyIdLogo />
        </v-img>
        </a>

        <v-spacer />
        
        <v-col cols="8">
          <v-row>
            <v-list v-model="selectedItem" color="transparent" >
              <v-list-item-group class="d-flex justify-space-around mt-2"  >
                <v-list-item
                  v-for="(item, i) in items"
                  :key="i"
                  :to="item.to"
                  router
                >
                  <v-list-item-content >
                    <v-list-item-title  v-text="item.title" style="color: white;"/>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-row>
        </v-col>

        <v-spacer />

        <v-btn
          @click.stop="rightDrawer = !rightDrawer"
          class="d-flex items-center flex-1 justify-center"
          color="#6D329D"
        >
          <v-text class="d-flex justify-space-around" style="color:white">Join Waiting List</v-text>
        </v-btn> 
      
      </v-col>
    </v-row>

    </v-app-bar>

    <!-- <BgHero /> -->
    <v-main  class="primary">
      <v-container>
        <Nuxt />
        <Feature class="mt-24"/>
      </v-container>
    </v-main>

    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import TourneyIdLogo from "../components/TourneyIdLogo.vue"
import Feature from "../pages/feature.vue"
export default {
    name: "DefaultLayout",
    components: { Feature },
    data() {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            items: [
                {
                    title: "Main Feature",
                    to: "/feature",
                    icon: null
                },
                {
                    title: "Popular Games",
                    to: "/inspire",
                    icon: null
                },
                {
                    title: "Blog",
                    to: "#",
                    icon: null
                },
                {
                    title: "Explore v",
                    to: "#",
                    icon: null
                }
            ],
            selectedItem: 1,
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: "tourney.id"
        };
    },
    components: { TourneyIdLogo }
}
</script>

<style scoped>

.columnHeader {
  align-content: center;
  align-items: center;
  justify-items: center;
  justify-content: space-around;
  float: none;
  margin: 0 auto;
  
}
.title {
  color: #6D329D;
  font-weight: bold;
  justify-content: center;
}

.active {
  color: #6D329D;
}
</style>
