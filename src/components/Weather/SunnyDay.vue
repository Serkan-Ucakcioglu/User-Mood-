<script setup lang="ts"></script>

<template>
  <!-- sunny group -->
  <div class="sunnys">
    <!-- Sun -->
    <div class="sun"></div>
    <div class="sun"></div>
    <div class="sun"></div>
  </div>
</template>
<style lang="scss" scoped>
//sunny
.sunnys {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 500px;
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
    -webkit-animation: rays 3s infinite;
    -moz-animation: rays 3s infinite;
    animation: rays 1s infinite;
  }
}

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
