<script setup lang="ts">
import { ref } from "vue";

const selected = ref(null);
</script>

<template>
  <section :class="selected">
    <div class="container">
      <select name="sec" v-model="selected">
        <option disabled value="">Please select one</option>
        <option value="cheerful">Cheerful</option>
        <option value="romantic">Romantic</option>
        <option value="gloomy">Gloomy</option>
        <option value="angry">Angry</option>
      </select>

      <div v-if="selected == 'cheerful'" class="sunnys">
        <div class="sun"></div>
        <div class="sun"></div>
        <div class="sun"></div>
      </div>
      <div  v-if="selected == 'romantic'" class="rains">
        <div class="rain"></div>
      </div>
      <div v-if="selected == 'gloomy'" class="cloud">
      <svg class="smallcloud" viewBox='0 0 100 100'>
    <path d="m 20 50 a 10 10 1 0 0 0 20 h 50 a 0.5 0.5 0 0 0 0 -25 a 0.5 0.5 0 0 0 -27 -3 a 0.5 0.5 0 0 0 -23 8 m 9 20 c 22 23 34 1 37 0 m 15 0" fill="white" />
  </svg>
  <svg class="smallcloud" viewBox='0 0 100 100'>
    <path d="m 20 50 a 10 10 1 0 0 0 20 h 50 a 0.5 0.5 0 0 0 0 -25 a 0.5 0.5 0 0 0 -27 -3 a 0.5 0.5 0 0 0 -23 8 m 9 20 c 22 23 34 1 37 0 m 15 0" fill="white" />
  </svg>
      </div>
    </div>
  </section>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

//section class 
.cheerful {
  background: linear-gradient(to bottom, #b9dfff, #4ba0db, #004390);
}
.gloomy{
    background: #2980b9;
}
 .romantic{
 background: linear-gradient(to bottom right, #131e35 ,#3f3a81);
}
.angry{
  background: red; 
}
////


section {
  display: flex;
  align-items: center;
  height: 100vh;

  .sunnys {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 500px;
  }
  select{
    height: 35px;
    border-radius: 4px;
  }
  .rains{
    width: 100%;
    height: 500px;
  }
  .cloud{
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 500px;
    svg{
      width: 100%;
      height: 100%;;
    }
  }
}


//  Romantic = Rainss

.rain{
  height: 100%;
  width: 100%;
  overflow: hidden;
  background-image: url("https://cdn.discordapp.com/attachments/744182992037216260/990016273008177242/rain1.png"),
  url("https://cdn.discordapp.com/attachments/744182992037216260/990016273217900584/rain2.png"),
  url("https://cdn.discordapp.com/attachments/744182992037216260/990016273456988240/rain3.png");
  
  animation: snow 1.5s linear  infinite ;
}

@keyframes snow {
  0% {
    background-position: 0px 0px, 0px 0px, 0px 0px;
  }
  100% {
    background-position: 500px 1000px, 400px 400px, 300px 300px;
  }
}
//



//CHERFUUL - SUNNY


.sun {
  display: block;
  height: 300px;
  width: 300px;
  margin-right: 15px;
  background: radial-gradient(
    rgba(255, 237, 175, 0.8) 50%,
    rgba(255, 237, 175, 0.2) 70%
  );
  border-radius: 50%;
  box-shadow: 0 0 0.5em rgba(255, 237, 175, 1);
  -webkit-animation: rays 10s infinite;
  -moz-animation: rays 10s infinite;
  animation: rays 10s infinite;
}

///

//responsive 
@media only screen and (max-width: 600px) {
  .sunnys {
    flex-direction: column !important;
    .sun {
      width: 200px !important;
      height: 200px !important;
      margin-top: 15px;
    }
  }
}
</style>
