<template>
    <div class="strip1">
        <div class="strip1-heading1">Staying healthy was just trial and error</div>
        <div class="strip1-heading2">Until Now</div>
        <v-btn  color="#fca001" rounded class="strip1-action">Get Started</v-btn>
    </div>
</template>
<script>
export default {
    name: 'Banner',
}
</script>

<style scoped>
.strip1{
  position:relative;
  background: url("../assets/fooddarzeestrip1.webp") bottom;
  width:100%;
  height: 100%;
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: #fff;
}
.strip1-heading1{
  font-size: 0.95em;
  font-weight: 500;
  line-height: 1.25;
}
.strip1-heading2{
  font-size: 2.15em ;
  font-weight: 800;
  margin: 0.5em 0;
}
.strip1-action{
  width: fit-content;
  color: #362e3d !important;
  align-self: center;
  line-height: 1.25;
  padding: 24px 29px 23px !important;
  font-weight: 700 !important;
}
@media screen and (min-width: 750px) and (max-width:1025px){
  .strip1-heading1 { font-size: 0.8em;}
  .strip1-heading2 { font-size: 1.6em;}
}
@media screen and (max-width: 750px){
  .strip1-heading1 { font-size: 0.9em;}
  .strip1-heading2 { font-size: 1em;}
}
</style>

