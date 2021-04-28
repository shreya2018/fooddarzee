<template>
<div>
    <h3 class="strip7-heading1 strip7-heading1-responsive">Eat Tasty <br/><span style="color:rgb(252, 212, 10)"> Daily Healthy</span></h3>
    <div class="strip7">
        <div class="sub-strip7">
            <div class="sub2-strip7">
                <div class="tmn-column">
                <img :src="require('../assets/strip7SubImage.webp')"/>
                </div>
                <div class="tmn-column">
                    <h3 class="strip7-heading1">Eat Tasty <br/><span style="color:rgb(252, 212, 10)"> Daily Healthy </span></h3>
                        <h6>The Ketogenic Diet</h6>
                        <p>
                        This is a high fat moderate protein diet with minimal carbs. This is the fastest way to lose fat.
                        </p>
                        <h6>Flexible Eating</h6>
                        <p>
                        Flexible Eating allows you to indulge in your favourite foods as part of your eating plan. 
                        Each meal is macro counted and calorie counted to keep fit and also provide healthy tasty 
                        meals daily.                
                        </p>
                        <h6>The High Protein Low Carb Diet</h6>
                        <p>
                        This is a high protein diet which restricts the use of of sugary foods and uses substitutes 
                        for regular high carb ingredients.                
                        </p>
                        <v-btn color="#d13526" outlined rounded class="get-started-btn"><h4>Get Started</h4></v-btn>
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
.strip7{
    background: url("../assets/strip7BackgroundImage.webp");
    width:100%;
    min-height: 650px;
    position: relative;
    display: flex;
    background-size: contain;
    background-repeat: no-repeat;
}
.strip7-heading1{
  font-size: 0.8em;  
  margin: 1em 0.5em;
}
.strip7-heading1-responsive{
    display: none;
}
.sub-strip7{
    width: 100%;
    margin: 0 auto 0;
}
.sub2-strip7{
    display: flex;
    flex-wrap: wrap;
    margin-right: -15px;
    margin-left: -15px;
    justify-content: flex-end;
}
.dish-description-list{
    display: flex;
    flex-direction: column;
    padding: 0.5em;
}
.dish-description-list-item{
    display: flex;
    width: 100%;
    font-size:0.6em;
    font-weight: 800;
    margin: 0.3em ;
}
.item-unique{
    color: rgb(252, 212, 10);
    font-size:1em;
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
    left: 0;
    transform: translateY(-50%);
    width: 50%;
}
img{
    max-width: 100%;
    height: auto;
}

@media (min-width: 768px) and (max-width: 992px) {
   .sub-strip7{max-width: 720px;}
    
}
   

@media (min-width: 992px){
    .tmn-column{ flex: 0 0 50%; max-width: 50%;}
}
   
@media screen and (max-width:768px){
    .strip7-heading1 {display: none;}
    .strip7-heading1-responsive{ display: flex;}
    .sub2-strip7{margin:0 0 0 0}
    .sub2-strip7{ justify-content: flex-start;}
    p{font-size: 0.45em}
}

</style>