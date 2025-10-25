<script setup>
import{ onMounted, onUpdated } from 'vue';
import { ref } from 'vue';

onMounted(() => {
  console.log('App mounted');
});
onUpdated(() => {
  console.log('App updated');
});

const squareColor = ref('red');

const changeColor =() =>{
squareColor.value = '#' + Math.floor(Math.random() * 16777215).toString(16);
}
</script>
<template>
<button @click="changeColor">Genereaza Culoare</button>
<div class="square" :style="{ backgroundColor: squareColor }"></div>
</template>

<style scoped>
.square {
  margin-top: 20px;
  width: 100px;
  height: 100px;
  background-color: red;
  margin-left: 15px;
}
</style>
