<script setup lang="ts">
import { ref } from "vue";
import SunnyDay from "./Weather/SunnyDay.vue";
import RomanticDay from "./Weather/RomanticDay.vue";
import GloomyDay from "./Weather/GloomyDay.vue";

const selected = ref(null);
</script>

<template>
  <section :class="selected">
    <div class="container">
      <h1 v-if="selected == null ">How are you today ? </h1>
      <select name="sec" v-model="selected">
        <option disabled value="">Please select one</option>
        <option value="cheerful">Cheerful</option>
        <option value="romantic">Romantic</option>
        <option value="gloomy">Gloomy</option>
        <option value="angry">Angry</option>
      </select>

      <div class="weather">
        <SunnyDay v-if="selected == 'cheerful'" />
        <RomanticDay v-if="selected == 'romantic'" />
        <GloomyDay v-if="selected == 'gloomy'" />
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
.romantic {
  background: linear-gradient(to bottom right, #131e35, #3f3a81);
}
.gloomy {
  background: #2980b9;
}
.angry {
  background-image: url(https://i01.sozcucdn.com/wp-content/uploads/2020/06/23/iecrop/hortum-shuttr_16_9_1592921956.jpg);
  background-repeat: no-repeat;
  background-size: 100%;
}
////

section {
  display: flex;
  align-items: center;
  height: 100vh;

  select {
    height: 35px;
    border-radius: 4px;
    font-size: 16px;
    font-weight: bold;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    
    
  }
}
</style>
