<template>
    <div class="footer">
        <div>
            <h3>Use our App on any device</h3>
            <div class="app-information">  
                <v-btn outlined class="app-info">
                    <v-icon size="50px">mdi-apple</v-icon>
                    <div class="text">
                        <div class="text1">Download on the</div>
                        <div class="text2">APP Store</div>
                    </div>
                </v-btn>
                <v-btn outlined class="app-info">
                    <v-icon size="50px">mdi-android</v-icon>
                    <div class="text">
                        <div class="text1">Download on the</div>
                        <div class="text2">Google Play</div>
                    </div>
                </v-btn>
                <v-btn outlined class="app-info">
                    <v-icon size="50px">mdi-desktop-mac</v-icon>
                    <div class="text">
                        <div class="text1">Open in</div>
                        <div class="text2">Browser</div>
                    </div>
                </v-btn>
            </div>
        </div>
        <div class="footer-strip2" >
            <div class="footer-links">
            <div class="footer-links-item">
                <h5 class="footer-headings">FOOD DARZEE</h5>
                <div class="footer-content">
                    <img src="../../public/fooddarzeelogo.webp"/>
                    <br/>
                    Key to your health.
                </div>
            </div>
            <div v-for="i in footerData" :key="i.footer_heading" class="footer-links-item">
                <h5 class="footer-headings">{{i.footer_heading}}</h5>
                <div class="footer-content">
                    <ul style="list-style-type:none" v-for="j in i.footer_content" :key="j">
                        <li style="margin-bottom:1.5em">{{j}}</li>
                    </ul>
                </div>
            </div>
            </div>
            <div>
                <v-btn  color="#fca001" rounded class="strip1-action">Get Started</v-btn>
            </div>
            <div class="footer-links">
                <v-icon v-for="i in socialMedia" :key="i" class="social-media-icons" color="#ffffff">{{i}}</v-icon>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {
    name:'Footer',
    data(){
        return{
            footerData:[
             {footer_heading:'QUICK LINKS',footer_content:['Coached.Darzee','Baked.Darzee','Pricing','FAQS','WhyFoodDarzee?','VisualStories']}
            ,{footer_heading:'MEALS DELIVERED',footer_content:['Mumbai','Delhi&NCR','Pune','Bengaluru','Hyderabad']}
            ,{footer_heading:'RECENT ARTICLES',footer_content:['5 steps to follow in your skincare regime','5 Ways to Boost Metabolism and Lose Weight','Why you should measure food before cooking ?','Keto Pyaaz Paratha Recipe','How to lose post pregnancy weight ?']}

            ],
            socialMedia:['mdi-facebook','mdi-twitter','mdi-instagram','mdi-linkedin','mdi-youtube']
        }
    }
}
</script>

<style scoped>
.footer{
    margin-top: 1.5em;
}
.app-information{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 2em;
}
.app-info{
    display: flex;
    border: 2px solid rgb(252, 212, 10);
    color: #777;
    height: fit-content !important;
    padding: 0.5em 0.5em 0.5em !important;
    margin: 1em 1em 1em;
    width:18em;
    justify-content: flex-start;
}
.text{
    margin-left:0.5em;
    text-align: left;
}
.text1{
    font-size: 14px;
    
}
.text2{
    font-size: 24px;
}
.footer-strip2{
    background-color: #362e3d;
    width:100%;
    margin: 0 auto 0;
}
.footer-links{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.footer-links-item{
    padding-right: 30px;
    padding-left: 30px;
    text-align: left ;
}
.footer-headings{
    font-size:0.5em;
    margin:3em 0 1.5em 0;
    padding: 0 0 0 1.5em;
}
.footer-content{
    font-size:0.4em;
    color: white;
}
.strip1-action{
  width: fit-content;
  color: #362e3d !important;
  align-self: center;
  line-height: 1.25;
  padding: 24px 29px 23px !important;
  font-weight: 700 !important;
}
.strip1-action:hover{
    transform: scale(1.1);
}

.social-media-icons{
    margin:1em 0.5em 1em;
}

@media screen and (min-width: 750px) and (max-width:1025px){
.footer-links-item{text-align: center;}
h3{font-size:35px}
}
@media screen and (max-width: 750px){
.footer-links-item{text-align: center;}
h3{font-size:35px}
}

</style>