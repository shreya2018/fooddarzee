<template>
    <div class="strip4">
        <v-carousel
            cycle
            hide-delimiter-background
            height="fit-content"
            hide-delimiters
            interval="4000"
            class="carousel"
            :show-arrows="false"
        >
            <v-carousel-item>
                <div class="carousel2-item">
                    <h2>How It Works at Food Darzee</h2>
                    <p>Ever wondered how we customise your meals, personalise 
                        your food and deliver them to you? Here is an insiders look at how we function.</p>
                    <iframe width="100%" height="400px" src="https://www.youtube.com/embed/2gkMPqEss9E">
                    </iframe>

                </div>
            </v-carousel-item>
            <v-carousel-item>
                <div class="carousel2-item">
                    <h2>4 People, 4 Stories</h2>
                    <p>We asked 4 people to talk about their relationship with food & health...<br/>
                        Here is what they had to say...</p>
                    <iframe width="100%" height="400px" src="https://www.youtube.com/embed/ZWDYtV7OpfI?autoplay=1">
                    </iframe>
                </div>
            </v-carousel-item>
            <v-carousel-item>
                <div class="carousel2-item">
                    <h2>Friends we wished for - Alia Bhatt</h2>
                    <p>We are so excited that you've been a part of our journey and glad that we've been 
                        able to help you with your fitness journey</p>
                    <iframe width="100%" height="400px" src="https://www.youtube.com/embed/l9SsZrvSKsg?autoplay=1">
                    </iframe>
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
    name:'Carousel1'
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
@media screen and (max-width:1000px) {

}

</style>        