<script setup lang="ts">
  import { ref, computed } from "vue";

  const msg = ref("こんにちは世界");
  const msgTextRed = ref("red");
  const msgBigColor = ref("black");
  const msgTextColor = ref("white");
  const msgStyles = ref({
    color: "white",
    backgroundColor: "black"
  });
  const msgStyles2 = ref({
    fontSize: "24pt"
  });
  const msgStyles3 = ref({
    color: "pink",
    fontSize: "24pt"
  });
  const textSize = computed(
    (): string => {
      const size = Math.round(Math.random() * 25) + 10;
      return `${size}pt`;
    }
  );
</script>

<template>
  <p v-bind:style="{color: msgTextRed}">
  {{ msg }}
  </p>
  <p v-bind:style="{color: 'pink'}">
  {{ msg }}
  </p>
  <p v-bind:style="{fontSize: textSize}">
  {{ msg }}
  </p>
  <p v-bind:style="{color: msgTextColor, backgroundColor: msgBigColor}">
  {{ msg }}
  </p>
  <p v-bind:style="{color: msgTextRed}">
  {{ msg }}
  </p>
  <p v-bind:style="{color: msgTextRed}">
  {{ msg }}
  </p>
  <p v-bind:style="{color: msgTextRed}">
  {{ msg }}
  </p>
  <p v-bind:style="{color: msgTextRed}">
  {{ msg }}
  </p>
</template>
