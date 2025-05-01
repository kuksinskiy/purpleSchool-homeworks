<script setup>
import TheHeart from "../assets/icons/TheHeart.vue";
const {score} = defineProps({
  score: Number
})

</script>

<template>
  <div class="score">
    <div class="score-value">{{score}}</div>
    <div class="score-icon"><TheHeart /></div>

  </div>

</template>

<style scoped>
.score {
  display: flex;
  align-items: center;
  padding: 12px 24px;
  border-radius: 36px;
  background: #CCE8FF;
  box-shadow: 0 0 4px 0 rgba(0, 0, 0, 0.15);
}
.score-value {
  color: #008BFE;
  font-size: 1rem;
  font-weight: 700;
  line-height: 24px;
  text-align: center;
  margin-right: 10px;
}
.score-icon {
  width: 24px;
  height: 24px;
}


</style>