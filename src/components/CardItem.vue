<script setup>
import { ref, watch } from 'vue'

defineProps({imgsrc : String, imgalttxt : String})

const flipClass = ref('')
function flipCard() {
  flipClass.value = flipClass.value === 'flip' ? '' : 'flip'
}
</script>

<template>
  <div class="card-container">
    <div class="scene" @click="flipCard">
      <div :class="`card ${flipClass}`">
        <div class="card__face card__face--front">
          <img :src="imgsrc" :alt="imgalttxt">
          <slot name="frontCardFace">
          </slot>
        </div>
        <div class="card__face card__face--back">
          <slot name="backCardFace"></slot>
        </div>
      </div>
      <div class="overlay"></div>
    </div>
  </div>
</template>

<style lang="scss">
/* card flip animation*/
@import '../assets/card-flip.scss';
</style>
