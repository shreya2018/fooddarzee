<template>
    <div class="strip8">
        <h2>So what's the catch?</h2>
        <p>There isn’t one. No tricky fine prints. No shady contracts. A no-nonsense weight loss/health gain 
            partner. Still not convinced? Read on…
        </p>
        <v-expansion-panels 
        accordion
        v-model="panel">
        <v-expansion-panel v-for="qa in QA" :key="qa.Q" class="qa-panel">
            <v-expansion-panel-header class="question-panel">
                {{qa.Q}}
                <template v-slot:actions>
                    <v-icon color="#d13526">
                    mdi-arrow-up
                    </v-icon>
                </template>
                </v-expansion-panel-header>
            <v-expansion-panel-content class="answer-panel">{{qa.A}}</v-expansion-panel-content>
        </v-expansion-panel>
    </v-expansion-panels>
    <v-btn color="#d13526" outlined rounded class="get-started-btn"><h4>Get Started</h4></v-btn>
    </div>
</template>

<script>
export default {
    name:'WhatsTheCatch',
    data(){
        return{
            QA:[{Q:"Why do I need to ‘subscribe’ to a plan? Why can’t I order everyday?",
                 A:"Eating healthy is a habit and that's why our meal plans start with minimum order of 3 days worth of meals to help you follow that habit."},
                 {Q:"Are there initiation fees or cancellation fees or other sneaky stupid fees?",A:"No. And there never will be."},
                 {Q:"Why should I trust you with such an important thing?",A:"With our team of expert chefs and nutritionists, we've helped more than 10000 people achieve their health goal. The Nutritionist guides you daily so that there's complete transparency and trust."},
                 {Q:"How many people have actually lost 10% body weight?",A:"3668 as of today, and counting"},
                 {Q:"Will my weight be maintained? I'm worried I'll gain it all back after the subscription ends",A:"We will be weaning you off the diet which will ensure that you don’t put too much weight back. If you follow our guidelines to the T, you'll not face any problems. The general weight gain due to water retention is 500-750 grams. Don't worry, we are with you even after you have completed your subscription."},
                 {Q:"What if I want to change the number of meals that I take in a day in my ongoing subscription?",A:"We will be adjusting the number of days in your current subscription based on the equivalent amount(₹) of the number of days pending and the rate of the new meal configuration. E.g if you subscribe for 30 days 4 meals a day configuration (Total Cost - ₹28500) and after 15 days decide to just opt for 3 meals. You will have ₹14250(28500x15/30) as a balance. The 3 Meals a Day rate is Rs 833. This means you will get 17 days (Rs 14,166) of 3 Meals as against 15 days of 4 Meals."},
                 {Q:"What is the refund policy?",A:"We will initiate a refund for the remaining number of days. The amount refunded will depend on your subscription plan and the number of days consumed which will be informed to you before confirming the cancellation. The refund will be processed within 10 working days of receiving the account details. E.g If you subscribed for 30 days and all 4 meals for ₹28,500 and consumed only 15 days it will be considered as a 15-day subscription(which costs ₹16150) and we will be refunding ₹12,350."}
                 ],
            panel:0,
        }
    }
}
</script>

<style scoped>
h2{
    margin: 1em 0 0 0 ;
    color:rgb(252, 212, 10)
}
p{
    font-size: 0.5em;
    margin: 4em 25% 6em !important;
}
.qa-panel{
    margin:0.5em 0.5em ;
    padding: 0.3em;
    width: 50%;
}
.question-panel{
    height:fit-content;
    font-size:0.6em;
    font-weight:700;
    line-height: 1.5;
}
.answer-panel{
    font-size:0.5em;
    text-align: left;
}
.get-started-btn{
    margin: 0 1em;
    width: fit-content;
}
@media screen and (min-width: 750px) and (max-width:1025px){
  h2{font-size:1.2em}
  .question-panel{ font-size: 0.5em;}
  .answer-panel { font-size: 0.4em;}
}
@media screen and (max-width: 750px){
    h2{font-size:1em}
  .question-panel{ font-size: 0.5em;}
  .answer-panel { font-size: 0.4em;}
}
</style>