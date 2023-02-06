<script setup>
import { ref } from "vue";
const count = ref(0);

console.log(count);

const add = () => {
  console.log("Pressing add button");
  count.value++;
}
const subtract = () => {
  console.log("Pressing subtract button");
  count.value--;
}
</script>

<template>
  <main>
    <div>
      <h4>The current count...</h4>
      <h1>{{ count }}</h1>
      <button @click="subtract()">-</button>
      <button @click="add()">+</button>
    </div>
  </main>
</template>

<style scoped>
  main {
    background-color: aliceblue;
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  div {
    text-align: center;
  }
</style>