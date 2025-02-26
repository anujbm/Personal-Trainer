<script setup lang="ts">
defineProps({
    user: Object
})

</script>
<template>
    <h1 class="text-2xl text-center font-bold p-2 w-full text-red-400">Fitness Program for {{ user.name }}</h1>
    <hr class="w-full" />

</template>