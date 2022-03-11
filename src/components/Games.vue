<script setup>
import GameItem from './GameItem.vue'
import Chess from './icons/Chess.vue'
import StreetFigther from './icons/StreetFighter.vue'
import Dota from './icons/Dota.vue'
import Minecraft from './icons/Minecraft.vue'
import Versus from './icons/Versus.vue'
</script>

<template>
  <GameItem imgsrc="/src/assets/chess.jpg" imgalttxt="Chess Banner">
    <template #icon>
      <Chess />
    </template>
    <template #frontImg></template>
    <template #heading>Chess Hype</template>

    What are your thoughts about Chess in general?<br />
    If you follow or participate in the recent <a href="javascript:void(0);">chess frenzy</a>,
    what do you think about it?
  </GameItem>

  <GameItem imgsrc="/src/assets/street-fighter.png" imgalttxt="Street Fighter Banner">
    <template #icon>
      <StreetFigther />
    </template>
    <template #heading>Street Fighter: "Ready... Fight!" </template>

    Do you prefer playing video games in <a href="javascript:void(0);">console</a> or <a href="javascript:void(0);">PC</a>?
  </GameItem>

  <GameItem imgsrc="/src/assets/dota.webp" imgalttxt="DOTA Banner">
    <template #icon>
      <Dota />
    </template>
    <template #heading>DOTA: "OWNING~"</template>

    Given that your financial needs will be guaranteed, will you choose to become a <a href="javascript:void(0);">professional esports player</a> + <a href="javascript:void(0);">twitch streamer</a> for life?
  </GameItem>

  <GameItem imgsrc="/src/assets/minecraft.jpg" imgalttxt="Minecraft Banner">
    <template #icon>
      <Minecraft />
    </template>
    <template #heading>Minecraft: "Never dig straight. Down. Or up." </template>

    "What you spend years building may be destroyed overnight. <a href="javascript:void(0);">Build anyway</a>."
    What do you think about this minecraft quote? Inspirational, random cheesy thought, or {fill in the blank}?
  </GameItem>

  <GameItem imgsrc="/src/assets/uno-vs-monopoly.png" imgalttxt="UNO VS Monopoly Banner">
    <template #icon>
      <Versus />
    </template>
    <template #heading>UNO vs Monopoly</template>

    Which one will you <a href="javascript:void(0);">choose to play</a>, if you cannot play the other one for the rest of your life?
  </GameItem>
</template>
