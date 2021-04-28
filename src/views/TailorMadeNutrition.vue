<template>
<div>
    <h3 class="strip5-heading1 strip5-heading1-responsive">Tailor Made Nutrition</h3>
    <div class="strip5">
        
        <div class="sub-background-img">
        <img :src="require('../assets/TailorMadeNutritionSubImage.webp')"/>
        </div>
        <div class="sub-strip5">
            <div class="sub2-strip5">
        <div class="tmn-column tmn-content"  >
            <h3 class="strip5-heading1">Tailor Made Nutrition</h3>
        <p>
            Each Food Darzee meal is tailored exactly to your requirements. The meals are prepared keeping 
            in mind your body type, gender, age, weight, height, medical conditions, preferences, lifestyle
             and fitness goal.
            <br/><br/>
            We provide meals for the Ketogenic diet, Low carb high protein diet and the Balanced Diet. Our 
            nutritionists make sure that every gram of food given to you is carefully measured so that you 
            eat exactly what you need to achieve your goals..
        </p>
        <v-btn color="#d13526" outlined rounded class="get-started-btn"><h4>Get Started</h4></v-btn>
        </div>
        <div class="tmn-column">
            <ul class="tmn-list">
                <li class="tmn-list-item">
                    <div class="tmn-list-icon">
                        <v-icon color="#fff">mdi-check</v-icon>
                    </div> 
                    <span style="margin-left:0.7em">1250 CALORIES</span>
                </li>
                <li class="tmn-list-item">
                    <div class="tmn-list-icon">
                        <v-icon color="#fff">mdi-check</v-icon>
                    </div> 
                    <span style="margin-left:0.7em">CONTINENTAL ONLY</span>
                </li>
                <li class="tmn-list-item">
                    <div class="tmn-list-icon">
                        <v-icon color="#fff">mdi-check</v-icon>
                    </div> 
                    <span style="margin-left:0.7em">VEG TUESDAYS</span>
                </li>
                <li class="tmn-list-item">
                    <div class="tmn-list-icon">
                        <v-icon color="#fff">mdi-check</v-icon>
                    </div> 
                    <span style="margin-left:0.7em">EXTRA SPICY</span>
                </li>
                <li class="tmn-list-item">
                    <div class="tmn-list-icon">
                        <v-icon color="#fff">mdi-check</v-icon>
                    </div> 
                    <span style="margin-left:0.7em">PRAWN ALLERGY</span>
                </li>
            </ul>
        </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.strip5{
    background: url("../assets/TailorMadeNutritionBackgroundImage.webp");
    background-size: contain;
    background-repeat: no-repeat;
    width:100%;
    min-height: 650px;
    position: relative;
    display: flex;
}
.strip5-heading1{
  font-size: 0.8em;  
  margin: 1em 0.5em;
}
.strip5-heading1-responsive{
    display: none;
}
.sub-strip5{
    /* max-width: 720px; */
    width: 100%;
    margin: 0 auto 0;
}
.sub2-strip5{
    display: flex;
    flex-wrap: wrap;
    margin-right: -15px;
    margin-left: -15px;
}

.tmn-column{
    position: relative;
    width: 100%;
    padding-right: 15px;
    padding-left: 15px;
}
p{
    font-size: 0.5em;
    padding:1em;
    text-align: left;
}
.get-started-btn{
    margin: 0 1em;
    width: fit-content;
}
.sub-background-img{
    position: absolute;
    top:50%;
    right: 0;
    transform: translateY(-50%);
    width: 25%;
}
img{
    max-width: 100%;
    height: auto;
}
.tmn-list{
    list-style-type: none;
    color: #fff;
    margin: 3em 0 0 0;
    text-align: left;
    width: 70%;
}
.tmn-list-icon{
    background-color: #fcd40a;
    width: 3em ;
    padding: 0.2em;
    height: inherit;
    display: flex;
    justify-content: center;
    align-items: center;
}
.tmn-list-item{
    background-color: #362e3d;
    margin: 0 0 1.5em 0 ;
    font-size:0.5em;
    /* width: 60%; */
    display: flex;
    font-weight: 600;
    align-items: center;
}
/* @media (min-width: 768px) and (max-width: 1279.98px) {
  
   
   
} */
@media (min-width: 992px){
    .tmn-column{ flex: 0 0 50%; max-width: 50%;}
}
/* @media screen and (max-width:992px){
    
} */
@media screen and (min-width: 750px) and (max-width:1025px){
    .strip5-heading1 {display: none;}
    .strip5-heading1-responsive{ display: flex;}
    .sub-strip5{max-width: 720px;}
    .sub2-strip5{flex-direction: column-reverse; margin:-2em 0 -2em 0;justify-content: flex-start; }
    .tmn-list{width: 100%;}
    p{font-size: 0.45em}
}
@media screen and (max-width: 750px){
    .strip5-heading1 {display: none;}
    .strip5-heading1-responsive{ display: flex;}
    .sub2-strip5{flex-direction: column-reverse;margin:0 0 0 0;justify-content: flex-start;}
    .tmn-list-item{height:3em; margin: 0 0 2.5em 0 ;}
    .tmn-content{ margin-top: 3.5em;}
    .tmn-list{width: 100%;}
    .sub-background-img{width: 50%;}
    p{font-size: 0.45em}

}
</style>