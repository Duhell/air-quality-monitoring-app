<script setup>
  import chartNav from "./chartNav.vue";

</script>

<template>
  <div class="h-full  max-w-[700px] w-full">
    <chartNav class="w-full"/>
    <div class="bg-[#152340] h-[325px] w-full p-4 rounded" id ="wrapper">
      <canvas id="thisChart"  class="w-full h-full ml-5" @msg="dataTransfer"></canvas>
    </div>
  </div>
</template>

