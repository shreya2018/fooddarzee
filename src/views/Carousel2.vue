<template>
    <div class="strip4">
        <v-carousel
            v-model="cmodel"
            :cycle="cycle"
            hide-delimiter-background
            height="fit-content"
            hide-delimiters
            interval="7000"
            class="carousel"
            :show-arrows="false"
        >
            <v-carousel-item eager>
                <div class="carousel2-item">
                    <h2>How It Works at Food Darzee</h2>
                    <p>Ever wondered how we customise your meals, personalise 
                        your food and deliver them to you? Here is an insiders look at how we function.</p>
                     <div id="player1" class="video"></div>

                </div>
            </v-carousel-item>
            <v-carousel-item eager>
                <div class="carousel2-item">
                    <h2 >4 People, 4 Stories</h2>
                    <p>We asked 4 people to talk about their relationship with food & health...<br/>
                        Here is what they had to say...</p>
                     <div id="player2" class="video"></div>
                </div>
            </v-carousel-item>
            <v-carousel-item eager>
                <div class="carousel2-item">
                    <h2>Friends we wished for - Alia Bhatt</h2>
                    <p>We are so excited that you've been a part of our journey and glad that we've been 
                        able to help you with your fitness journey</p>
                    <div id="player3" class="video"></div>
                </div>
            </v-carousel-item>
        </v-carousel>
        <div>
            
        <v-btn color="#d13526" outlined rounded class="get-started-btn"><h4>Get Started</h4></v-btn>
        </div>
    </div>
</template>

<script>
export default {
    name:'Carousel2',
    data(){
        return{
            cmodel:null,
            cycle:true,
            videoHeight:'390px',
            videoWidth:'640px',
            flag:null,
            temp:0
        }
    },

    watch:{
        
        cmodel:function(n){
            var YouTubeIframeLoader = require('youtube-iframe');
            var that = this
            if(n===1){
               YouTubeIframeLoader.load(function(YT) { new YT.Player('player3', {height: '390px',
                    width: '100%',
                    videoId: 'l9SsZrvSKsg',
                    events: {
                        'onStateChange':that.onPlayerStateChange
                    }
                    });})
            }
            if(n===0){
               YouTubeIframeLoader.load(function(YT) { new YT.Player('player2', {height: '390px',
                    width: '100%',
                    videoId: 'ZWDYtV7OpfI',
                    events: {
                        'onStateChange':that.onPlayerStateChange
                    }
                    });})
            }
            if(n===2||n===0){
               YouTubeIframeLoader.load(function(YT) { new YT.Player('player1', {height: '390px',
                    width: '100%',
                    videoId: '2gkMPqEss9E',
                    events: {
                        'onStateChange':that.onPlayerStateChange
                    }
                    });})
            }
        }
    },
    methods:{
        onPlayerStateChange(x){
            console.log(x.data);
            if(x.data===1)
                this.cycle = false;
            if(x.data===2||x.data===0||x.data===-1)
                this.cycle = true;
        }
    }
}
</script>

<style scoped>
.strip4{
  width:100%;
  height: 100%;
  text-align: left;
  padding: 1em 0;
}
.carousel2-item{
    text-align: center;
}

h2{
    color:rgb(252, 212, 10);
}
p{
    color:#362e3d ;
    font-size: 0.5em;
    width: 40%;
    margin: 3em auto 2em !important;
}

.responsive {
  max-width: 100%;
  height: auto;
  
}

.get-started-btn{
    margin: auto 2em;
   
}
@media screen and (min-width: 750px) and (max-width:1025px){
  h2{font-size:1.2em}
 

}
@media screen and (max-width: 750px){
    h2{font-size:1em; }
    

}


</style>        