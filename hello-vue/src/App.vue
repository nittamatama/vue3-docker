<script setup lang="ts">
  import { ref } from "vue";

  const url = ref("https://vuejs.org/");
</script>

<template>
  <p><a v-bind:href="url" target="_blank">Vue.jsサイト</a></p>
  <p><a :href="url" target="_blank">Vue.jsサイト省略形</a></p>
  <p><a v-bind:href="url + 'guide/introduction.html'" target="_blank">Vue.jsガイド</a></p>
</template>
