<script setup lang="ts">
import { ref } from "vue";
import Header from './Components//Header.vue'
import CardGrid from './Components/CardGrid.vue'
import Card from './Components/Card.vue'
const user = {
  name: "Anuj Magar"
}

const exercises = ref([
  { name: 'Pushups', quantity: 20 },
  { name: 'Situps', quantity: 20 },
  { name: 'Squats', quantity: 40 },
])
// import { invoke } from "@tauri-apps/api/core";

// const greetMsg = ref("");
// const name = ref("");

// async function greet() {
//   // Learn more about Tauri commands at https://tauri.app/develop/calling-rust/
//   greetMsg.value = await invoke("greet", { name: name.value });
// }


</script>

<template>
  <main class="w-full">
    <Header :user="user" />


    <h2 class="w-full p-4 text-center text-xl">Today's Summary</h2>
    <CardGrid class="p-4">
      <Card v-for="(exercise, index) in exercises" :key="index">
        {{ exercise.name }} : {{ exercise.quantity }}
      </Card>
    </CardGrid>


  </main>
</template>

<style scoped></style>