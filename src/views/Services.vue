<template>
    <div class="strip2">
        <h2 class="strip2-heading1">What you get</h2>
        <div class="service-list">
            <div class="service">
                <img :src ="require('../assets/PersonalizedNutrionist.webp')"/>
                <div class="icon-sub-heading">Personalized Nutritionist</div>
            </div>
            <div class="service">
                <img :src="require('../assets/TastyMeals.webp')"/>
                <div class="icon-sub-heading">Tasty Meals</div>
            </div>
            <div class="service">
                <img :src="require('../assets/DoorstepDelivery.webp')"/>
                <div class="icon-sub-heading">Doorstep Delivery</div>
            </div>
            <div class="service">
                <img :src="require('../assets/WeeklyHealth.webp')"/>
                <div class="icon-sub-heading">Weekly Health</div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    name:'Services'
}
</script>

<style scoped>
.strip2{
    background-color: rgb(244, 243, 243);
    padding: 50px 15px 40px;
    height: fit-content;
}
.strip2-heading1{
    font-size: 1.3em; 
}
.service-list{
    display: flex;
    justify-content: space-evenly;
    margin: 2em 1.5em;
    flex-wrap: wrap;
}
.service{
    margin:0.5em;
    width: 20%;
}
.icon-sub-heading{
    font-size: 0.5em;
}
@media screen and (max-width: 750px){
    img{ transform: scale(0.8);}
    .service-list{ margin: 2em 0.5em;}
    .service{ width: 35%;}
}


</style>