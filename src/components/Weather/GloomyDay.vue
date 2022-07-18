<script setup lang="ts"></script>

<template>
  <div class="cloud">
    <svg class="smallcloud" viewBox="0 0 100 100">
      <path
        d="m 20 50 a 10 10 1 0 0 0 20 h 50 a 0.5 0.5 0 0 0 0 -25 a 0.5 0.5 0 0 0 -27 -3 a 0.5 0.5 0 0 0 -23 8 m 9 20 c 22 23 34 1 37 0 m 15 0"
        fill="white"
      />
    </svg>
    <svg class="smallcloud" viewBox="0 0 100 100">
      <path
        d="m 20 50 a 10 10 1 0 0 0 20 h 50 a 0.5 0.5 0 0 0 0 -25 a 0.5 0.5 0 0 0 -27 -3 a 0.5 0.5 0 0 0 -23 8 m 9 20 c 22 23 34 1 37 0 m 15 0"
        fill="white"
      />
    </svg>
  </div>
</template>
<style lang="scss">
.cloud {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 500px;
  svg {
    width: 100%;
    height: 100%;
  }
}
</style>
