<script setup lang="ts"></script>

<template>
  <div class="rains">
    <div class="rain"></div>
  </div>
</template>

<style scoped>
.rains {
  width: 100%;
  height: 500px;
}

.rain {
  height: 100%;
  width: 100%;
  overflow: hidden;
  background-image: url("https://cdn.discordapp.com/attachments/744182992037216260/990016273008177242/rain1.png"),
    url("https://cdn.discordapp.com/attachments/744182992037216260/990016273217900584/rain2.png"),
    url("https://cdn.discordapp.com/attachments/744182992037216260/990016273456988240/rain3.png");

  animation: snow 1.5s linear infinite;
}

@keyframes snow {
  0% {
    background-position: 0px 0px, 0px 0px, 0px 0px;
  }
  100% {
    background-position: 500px 1000px, 400px 400px, 300px 300px;
  }
}
</style>
