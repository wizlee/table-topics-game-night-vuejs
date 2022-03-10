<script setup>
const props = defineProps(['imgSrc, imgAltTxt'])
</script>

<template>
  <div class="card-container">
    <div class="scene">
      <div class="card">
        <div class="card__face card__face--front">
          <img v-if="imgAltTxt" src="{{imgSrc}}" alt="{{imgAltTxt}}" srcset="" :key="imgAltTxt">
          <slot name="frontCardFace">
          </slot>
        </div>
        <div class="card__face card__face--back">
          <slot name="backCardFace"></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
/* card flip animation*/
@import '../assets/card-flip.scss';
</style>
