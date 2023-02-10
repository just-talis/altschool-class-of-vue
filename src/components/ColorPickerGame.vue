<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script setup>
import { ref, reactive } from "@vue/reactivity";
import { useMatchColour } from "../composables/useMatchColour";


const colors = ["green", "red", "blue", "purple"];
const { message, matchColor } = useMatchColour(colors);

//export default {
//setup() {
// const colors = ["green", "red", "blue", "purple"];
//const {message, matchColor} = useMatchColour(colors);
// return { colors, message, matchColor };
//},
//};
</script>

<style></style>
