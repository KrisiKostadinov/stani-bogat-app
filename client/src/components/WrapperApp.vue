<template>
  <div v-if="!backgroundMusic.isPlaying" class="icon" @click="backgroundMusic.play" v-html="icons.playIcon"></div>
  <div v-else class="icon" @click="backgroundMusic.stop" v-html="icons.pauseIcon"></div>
  <slot></slot>
</template>

<script>
import { musics, icons } from "../constats";
import { useSound } from "@vueuse/sound";
import { ref } from "vue";

export default {
  name: "WrapperApp",
  setup() {
    const randomNumber = Math.floor(Math.random(4) * 4);
    const backgroundMusic = ref(useSound(musics[randomNumber]));
    return { backgroundMusic, icons }
  }
}
</script>