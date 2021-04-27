<template>
<!-- <v-container class="py-0 fill-height"> -->
  <div class="menu-bar">
    <div class="menu-items menu-item1">
      <div>Pricing</div>
      <div>Blogs</div>
      <div>FAQs</div>
    </div>
    <img src="../../public/fooddarzeelogo.webp" class="logo"/>
      <div class="menu-items menu-item2">
        <div><v-icon class="phone-icon" color="#000" >mdi-phone</v-icon><span class="phone">+91 9590510520</span></div>
        <v-btn outlined color="#d13526" rounded class="get-started-btn">Get Started</v-btn>
      </div>
    </div>
<!-- </v-container> -->
</template>

<script>
export default {
  name: 'MenuBar',
  props: {
  
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .menu-bar{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .menu-items{
    font-size: 0.5em;
    font-weight: 700;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width:28%;
    flex-wrap: wrap;
  }

  .logo{
    width: 3.75em;
    height: 3.75em;
  }

  .phone-icon{
    transform: scale(0.8);
  } 
  .get-started-btn{
    border-width: 2px;
    font-weight: 700;
  }
 .get-started-btn:hover{
  background-color: #d13526 ;
  color: white !important;
  }

  @media screen and (max-width: 1070px){
    .menu-item2 { justify-content: flex-end; }
    .get-started-btn { margin-top: 0.25em;} 
  }
  @media screen and (max-width: 750px){
    .menu-item2 {justify-content: center; width:60%}
    .menu-item1 { display:none }
    .logo{ 
      width: 1.75em;
      height:1.75em;
    }
    .phone{ display:none }
    .phone-icon {transform: scale(1.1);}
    .get-started-btn {transform: scale(0.8);}
  }


</style>
