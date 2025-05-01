<script setup>

const emit = defineEmits({
  changeStatus(payload) {},
  flipCard() {}
})

function flip() {
  emit('flipCard')
}

</script>

<template>

  <div class="card" @click="flip">
    <div class="card-border"></div>
    <div class="card-number">01</div>
    <div class="card-text">unadmitted</div>
    <div class="card-flip">ПЕРЕВЕРНУТЬ</div>
  </div>

</template>

<style scoped>

.card {
  width: 250px;
  height: 376px;
  border-radius: 16px;
  background: #FFF;
  box-shadow: 0 0 16px 0 rgba(0, 0, 0, 0.10);
  position: relative;
}

.card-border {
  position: absolute;
  top: 28px;
  left: 19px;
  right: 19px;
  bottom: 28px;
  border-radius: 12px;
  border: 1px solid #CCE8FF;
}

.card-number, .card-flip {
  position: absolute;
  background-color: var(--color-primary);

  text-align: center;

  line-height: normal; /* 150% */
}

.card-number {
  top: 20px;
  left: 35px;
  font-size: 14px;
  font-weight: 400;
}

.card-flip {
  bottom: 19px;
  left: 50%;
  transform: translateX(-50%);
  letter-spacing: 0.09rem;
  font-size: 12px;
  font-weight: 700;
  line-height: 18px;
}

.card-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 1.125rem;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

</style>