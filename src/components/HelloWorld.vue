<script setup lang="ts">
import { ref } from "vue";

const selected = ref(null);
</script>

<template>
  <section class="sunny">
    <div class="container">
      <select name="sec" v-model="selected">
        <option disabled value="">Please select one</option>
        <option value="Cheerful">Cheerful</option>
        <option value="Romantic">Romantic</option>
        <option value="Gloomy">Gloomy</option>
        <option value="Angry">Angry</option>
      </select>

      <div class="weather">
        <div class="sun"></div>
        <div class="sun"></div>
        <div class="sun"></div>
      </div>
    </div>
  </section>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
section {
  display: flex;
  align-items: center;
  height: 100vh;

  .weather {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 500px;
  }
}

.sunny {
  background: linear-gradient(to bottom, #b9dfff, #4ba0db, #004390);
}

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
@media only screen and (max-width: 600px) {
  .weather {
    flex-direction: column !important;
    .sun {
      width: 200px !important;
      height: 200px !important;
      margin-top: 15px;
    }
  }
}
</style>
