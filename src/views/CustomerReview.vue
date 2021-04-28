<template>
    <div class="strip8">
        <h2>Returns >>> Investment</h2>
        <p>Whatever we say here will surely sound insincere. We’d rather let our customers do the talking.</p>
        <v-slide-group
            show-arrows
        >
            <v-slide-item
                v-for="customer,index in reviews"
                :key="customer.customer_name"
            >
                <div>
                <img :src="require('../assets/customer'+ (index+1) +'.webp')" class="customer-img">
                <v-card
                class="review-card"
                tile
                >
                <div>{{customer.customer_review}}</div>
                    <br>
                <div class="sub-heading1 sub-heading2">{{customer.customer_name}}, {{customer.customer_age}}</div>
                <div class="sub-heading2">{{customer.customer_occupation}}</div>
                </v-card>
                </div>
            </v-slide-item>
    </v-slide-group>
    <div class="sub-heading">See? It's a no brainer. Do it.</div>
    <v-btn color="#d13526" outlined rounded class="get-started-btn"><h4>Get Started</h4></v-btn>
    </div>
</template>

<script>
export default {
    name:'CustomerReview',
    data(){
        return{
            reviews:[{customer_img:'../assets/customer1.webp', customer_name:'Parag Kamble', customer_age:'37', customer_occupation:'Management Consultant', customer_review:`“Can't believe how many ways you guys can make paneer! I also loved the regular keto desserts!”`},
            {customer_img:'../assets/customer2.webp', customer_name:'Zeenia Wadia', customer_age:'29', customer_occupation:'Marketing Specialist', customer_review:`“I've lost 9 kgs in 2 months! Sustained weight loss, heightened confidence, mother-like customer service. It’s a bargain.”`},
            {customer_img:'../assets/customer3.webp', customer_name:'Tina Kanjani', customer_age:'36', customer_occupation:'Housewife', customer_review:`“Food Darzee took care of my extreme likes and dislikes as if I was a celebrity.”`}

            ]
        }
    }
}
</script>

<style scoped>
.strip8
{
    margin-bottom: 2em;
}
h2{
    margin: 1em 0 0 0 ;
    color:rgb(252, 212, 10)
}
p{
    font-size: 0.5em;
    margin: 4em 25% 2em !important;
}
.review-card{
    background-color: #362e3d !important;
    background-image: url('../assets/customerReviewBGImage.webp');
    background-size: contain;
    height: fit-content;
    width: 400px;
    margin: 0 0.5em 0;
    padding: 6em 0.5em ;
    color: #fff !important;
    font-size: 0.6em;
}
.customer-img{
    transform: translateY(50%);
    position: relative;
    z-index: 2;
}
.sub-heading1{
    font-weight: 500 !important;
}
.sub-heading2{
    font-size: 0.9em !important;
    font-weight: 400;
}
.sub-heading{
    font-size:0.76em;
    margin-top: 1em;

}
.get-started-btn{
    margin: 0 1em;
    width: fit-content;
}

@media screen and (min-width: 750px) and (max-width:1025px){
  h2{font-size:1.2em}
  .review-card{width: 350px;font-size: 0.4em;}

}
@media screen and (max-width: 750px){
    h2{font-size:1em; }
    .review-card{width: 250px;font-size: 0.4em;}

}

</style>