<script setup>
import GameItem from './GameItem.vue'
import Chess from './icons/Chess.vue'
import StreetFigther from './icons/StreetFighter.vue'
import Dota from './icons/Dota.vue'
import Minecraft from './icons/Minecraft.vue'
import Versus from './icons/Versus.vue'
</script>

<template>
  <GameItem :imgSrc="'../assets/street-fighter.png'" :imgAltTxt="'Knight'">
    <template #icon>
      <Chess />
    </template>
    <template #frontImg></template>
    <template #heading>Chess Hype</template>

    Vue's
    <a target="_blank" href="https://vuejs.org/">official documentation</a>
    provides you with all information you need to get started.
  </GameItem>

  <GameItem>
    <template #icon>
      <StreetFigther />
    </template>
    <template #heading>Street Fighter: "Ready! Fight!" </template>

    This project is served and bundled with
    <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite</a>. The recommended IDE
    setup is <a href="https://code.visualstudio.com/" target="_blank">VSCode</a> +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>. If you need to test
    your components and web pages, check out
    <a href="https://www.cypress.io/" target="_blank">Cypress</a> and
    <a href="https://docs.cypress.io/guides/component-testing/introduction" target="_blank"
      >Cypress Component Testing</a
    >.

    <br />

    More instructions are available in <code>README.md</code>.
  </GameItem>

  <GameItem>
    <template #icon>
      <Dota />
    </template>
    <template #heading>DOTA: "OWNING~"</template>

    Get official tools and libraries for your project:
    <a target="_blank" href="https://pinia.vuejs.org/">Pinia</a>,
    <a target="_blank" href="https://router.vuejs.org/">Vue Router</a>,
    <a target="_blank" href="https://test-utils.vuejs.org/">Vue Test Utils</a>, and
    <a target="_blank" href="https://github.com/vuejs/devtools">Vue Dev Tools</a>. If you need more
    resources, we suggest paying
    <a target="_blank" href="https://github.com/vuejs/awesome-vue">Awesome Vue</a>
    a visit.
  </GameItem>

  <GameItem>
    <template #icon>
      <Minecraft />
    </template>
    <template #heading>Minecraft: "Never dig straight. Down. Or up." </template>

    "What you spend years building may be destroyed overnight. <a href="javascript:void(0);">Build anyway</a>."
    What do you think about this minecraft quote? Inspirational, random cheesy thought, or {fill in the blank}?
  </GameItem>

  <GameItem>
    <template #icon>
      <Versus />
    </template>
    <template #heading>UNO vs Monopoly</template>

    Which one will you <a href="javascript:void(0);">choose to play</a>, if you cannot play the other one for the rest of your life?
  </GameItem>
</template>
