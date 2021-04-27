<template>
  <v-app id="inspire">
    <header>
    <div class="padding-constraint">
      <v-btn rounded color="#362e3d" class="menu-btn" @click="drawer=true"><v-icon>mdi-menu</v-icon></v-btn>
      <div>
        <MenuBar />
      </div>
    </div>
    <v-navigation-drawer
      app
      clipped
      right
      v-model="drawer"
      class="navigation-bar"
    >
      <div class="navigation-close-icon">
        <v-icon color="#ffffff" @click="drawer=false">mdi-close</v-icon>
      </div>
      <v-list>
        <v-list-item
          v-for="item in navigationDrawerContent"
          :key="item"
          link
        >
          <v-list-item-content>
            <v-list-item-title class="navigation-bar">{{item}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-content>
            <v-icon color="#ffffff">mdi-phone</v-icon>
            <v-icon color="#ffffff">mdi-facebook</v-icon>
            <v-icon color="#ffffff">mdi-instagram</v-icon>
            <v-btn outlined rounded color="#ffffff">Sign Up</v-btn>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    </header>
    <section id="strip1">
      <div class="padding-constraint remove-padding">
        <div class="strip">
          <Banner/>
        </div>
        <Services/>
        <Carousel1 />
        <Carousel2 />
        <TailorMadeNutrition/>
        <DishDescription/>
        <EatTastyEatHealthy/>
        <WhatsTheCatch/>
      </div>
    </section>
    
  </v-app>
</template>

<script>
import MenuBar from './components/MenuBar.vue'
import Banner from './views/Banner.vue'
import Services from './views/Services.vue'
import Carousel1 from './views/Carousel1.vue'
import Carousel2 from './views/Carousel2.vue'
import TailorMadeNutrition from './views/TailorMadeNutrition.vue'
import DishDescription from './views/DishDescription.vue'
import EatTastyEatHealthy from './views/EatTastyEatHealthy.vue'
import WhatsTheCatch from './views/WhatsTheCatch.vue'
export default {
  name: 'App',
  components: {
    MenuBar,
    Banner,
    Services,
    Carousel1,
    Carousel2,
    TailorMadeNutrition,
    DishDescription,
    EatTastyEatHealthy,
    WhatsTheCatch
  },
  data: () => ({
      links: [
        'Dashboard',
        'Messages',
        'Profile',
        'Updates',
      ],
      navigationDrawerContent:['Home','Why Food Darzee?','Pricing','Testimonials','Baked.Darzee','Coached.Darzee','FAQS','Blog','About','Contact'],
      drawer:false,
    }),
  }
</script>
<style>
@font-face {
  font-family: "Quicksand";
  src: local("Quicksand"),
   url(./assets/fonts/Quicksand-VariableFont_wght.ttf) format("truetype");
}
#inspire{
  font-family: "Quicksand",sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-size: 32px;
}
header{
  position: fixed;
  width:100%;
  height: 3em;
  background-color: white;
  z-index: 10;
}
.padding-constraint{
padding: 0 6% 0 6%;
}
.menu-btn{
  color:white !important;
  width: fit-content;
  position:fixed !important;
  right:-1.2em;
  top:3em;
}
.navigation-bar{
  background-color: #362e3d !important;
  color: white !important;
}
.navigation-close-icon{
  display: flex;
  margin: 0.5em;
}
.v-list-item__content>*{
  flex: 1 1 !important;
}
.strip{
  height: 600px;
}

@media screen and (max-width: 750px){
  .menu-btn { transform: scale(0.8); top:1.7em}
  header { height:2.5em; padding-top: 0.4em;}
  .remove-padding { padding: 0;  }
  .strip { height: 500px;}
}

</style>