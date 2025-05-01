<script setup>
import TheScore from "./TheScore.vue";
import {ref} from "vue";

const score = ref(100)

</script>

<template>
  <header>
    <div>Запомни слово</div>
    <TheScore :score="score" />
  </header>

</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 121px;
}

</style>