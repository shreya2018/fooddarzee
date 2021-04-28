<template>
<div>
    <div class="strip6">
        <div class="sub-background-img">
        <img :src="require('../assets/strip6SubImage.webp')"/>
        </div>
        <div class="sub-strip6">
            <div class="sub2-strip6">
                <div class="tmn-column tmn-content"  >
                <div class="dish-description-list">
                    <div class="dish-description-list-item"><v-icon size="32px" color="#d13526">mdi-close-box-outline</v-icon><span style="margin-left:0.5em"> Mouth-watering</span></div>
                    <div class="dish-description-list-item"><v-icon size="32px" color="#d13526">mdi-close-box-outline</v-icon><span style="margin-left:0.5em"> Lip Smacking</span></div>
                    <div class="dish-description-list-item"><v-icon size="32px" color="#d13526">mdi-close-box-outline</v-icon><span style="margin-left:0.5em"> Finger-licking</span></div>
                    <div class="dish-description-list-item item-unique"><v-icon size="45px" color="rgb(252, 212, 10)">mdi-checkbox-marked</v-icon><span style="margin-left:0.5em"> All of the above</span></div>
                </div>
                <p>
                   Diets tend to be monotonous, this is why we believe in providing a lot of variety.
                    <br/><br/>
                    Our 4 week unique menu ensures that none of the dishes are repeated taking the monotony 
                    away from the diet.
                    <br/><br/>
                    Everything from your likes, dislikes to even certain allergies are considered before cooking 
                    meals for you.
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
.strip6{
    background: url("../assets/strip6BackgroundImage.webp");
    width:100%;
    min-height: 650px;
    position: relative;
    display: flex;
    background-size: contain;
    background-repeat: no-repeat;
}
.strip6-heading1{
  font-size: 0.8em;  
  margin: 1em 0.5em;
}
.strip6-heading1-responsive{
    display: none;
}
.sub-strip6{
    width: 100%;
    margin: 0 auto 0;
}
.sub2-strip6{
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
   .sub-strip6{max-width: 720px;}
    p{margin-top:15em;}
}
   

@media (min-width: 992px){
    .tmn-column{ flex: 0 0 50%; max-width: 50%;}
}
   
@media screen and (max-width:768px){
    .strip6-heading1 {display: none;}
    .strip6-heading1-responsive{ display: flex;}
    .sub2-strip6{margin:0 0 0 0}
    .sub2-strip6{ justify-content: flex-start;}
    p{margin-top:20em;font-size: 0.45em}
    .sub-background-img{width: 100%;}
}

</style>