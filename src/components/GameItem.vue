<script setup>
import CardItem from './CardItem.vue'
import { reactive, watch  } from 'vue'

const props = defineProps(['imgSrc, imgAltTxt'])
const state = reactive({imgSrc: props.imgSrc, imgAltTxt: props.imgAltTxt})
watch(state.imgAltTxt, (newVal, _) => {
  state.imgAltTxt = newVal
  console.log(`state.imgAltTxt= ${state.imgAltTxt}`)
})
watch(state.imgSrc, (newVal, _) => {
  state.imgSrc = newVal
})
</script>

<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <CardItem :imgSrc="imgSrc" :imgAltTxt="imgAltTxt">
        <template #frontCardFace>
          <slot name="frontImg"></slot>
        </template>
        <template #backCardFace>
          <h3>
          <slot name="heading"></slot>
        </h3>
        <slot></slot>
        </template>
      </CardItem>
    </div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  display: flex;
  --item-relative-ref: 100px;
}

.details {
  flex: 1;
  margin-left: 1rem;
  min-height: var(--item-relative-ref);
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  border: 1px solid var(--color-border);
  background: var(--color-background);
  border-radius: 8px;
  width: var(--item-relative-ref);
  height: var(--item-relative-ref);

  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 1rem 0 1rem calc(var(--section-gap) / 2);
    --item-relative-ref: 100px;
  }

  i {
    top: calc(50% - var(--item-relative-ref) / 2);
    left: -50px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: var(--item-relative-ref);
    height: var(--item-relative-ref);
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: 0;
    height: calc((100% - var(--item-relative-ref)) / 2);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: 0;
    height: calc((100% - var(--item-relative-ref)) / 2);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
