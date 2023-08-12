<script setup lang="ts">
  import { ref } from "vue";

  const msg = ref("まだです");
  const onEnterKey = (): void => {
    msg.value = "エンター気ーのうか";
  };
  const onRightButtonClick = (): void => {
    msg.value = "ボタンが右クリックされました";
  };
  const onShiftClick = (): void => {
    msg.value = "shiftキーを押しながらクリックされた";
  };
</script>

<template>
  <p>{{ msg }}</p>
  <input type="text" v-on:keydown.enter="onEnterKey"><br>
  <button v-on:click.right="onRightButtonClick">右クリック</button><br>
  <button v-on:click.shift="onShiftClick">shiftおしながら</button><br>
</template>

<style>
</style>
