<template>
  <button @click="sayWord" class="clickable">Say Word</button>
</template>

<script>
export default {
props: ["word"],

methods: {
    props: ["word"],
    sayWord() {
      const utterance = new SpeechSynthesisUtterance(this.word);
      speechSynthesis.speak(utterance);
    }
  },
}
</script>

<style>

</style>