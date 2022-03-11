<script setup>
defineProps({imgsrc : String, imgalttxt : String})
</script>

<template>
  <div class="card-container">
    <div class="scene">
      <div class="card">
        <div class="card__face card__face--front">
          <img :src="imgsrc" :alt="imgalttxt">
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
