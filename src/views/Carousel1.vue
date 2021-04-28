<template>
    <div class="strip3">
        <h3 class="strip3-heading1 strip3-heading1-responsive">What we do</h3>
        <v-carousel
            cycle
            hide-delimiter-background
            height="fit-content"
            hide-delimiters
            interval="4000"
            :show-arrows="false"
        >
            <v-carousel-item>
                <img class="responsive" src="../assets/KetoMeals.webp"/>
            </v-carousel-item>
            <v-carousel-item>
                <img class="responsive" src="../assets/VeganMeals.webp"/>
            </v-carousel-item>
            <v-carousel-item>
                <img class="responsive" src="../assets/LowCarbMeals.webp"/>
            </v-carousel-item>
            <v-carousel-item>
                <img class="responsive" src="../assets/BalancedMeals.webp"/>
            </v-carousel-item>
        </v-carousel>
        <div>
        <h3 class="strip3-heading1">What we do</h3>
        <p>
            We create and deliver custom meals for your body types to help you reach your goals.
            <br/><br/>
            The nutritionist assigned to you understands your lifestyle and charts out a course for you and 
            decides whether you have to follow the ketogenic diet, high protein low carb diet or the balanced 
            diet.
            <br/><br/>
            This is then communicated to the culinary team, who prepare calorie counted, macro counted meals 
            specifically for you.
            <br/><br/>
            We deliver 4 meals a day, ensuring that the meals are fresh and delivered at a location convenient 
            to you.
            <br/><br/>
            Your personal nutritionist acts like your mentor, follows up on a regular basis maps 
            your progress and tweaks and tailors your diet, shifting you between various diets 
            (ketogenic, low carb high protein, balanced)
        </p>
        <v-btn color="#d13526" outlined rounded class="get-started-btn"><h4>Get Started</h4></v-btn>
        </div>
    </div>
</template>

<script>
export default {
    name:'Carousel1'
}
</script>

<style scoped>
.strip3{
  background: url("../assets/strip3BackgroundImage.webp");
  width:100%;
  height: 100%;
  background-size: cover;
  display: flex;
  text-align: left;
  background-size: contain;
  background-repeat: no-repeat;
}
.strip3-heading1{
  font-size: 0.8em;  
  margin: 1em 0.5em;
}
.strip3-heading1-responsive{
    display: none;
}
.responsive {
  max-width: 100%;
  height: auto;
  
}

p{
    font-size: 0.5em;
    padding:1em;
}
.get-started-btn{
    margin: 0 1em;
}
@media screen and (max-width:1000px) {
    .strip3-heading1 {display: none;}
    .strip3 {flex-wrap: wrap;}
    .strip3-heading1-responsive {display: inline;}
    p{font-size: 0.45em}
}

</style>        