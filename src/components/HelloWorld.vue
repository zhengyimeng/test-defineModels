<script setup lang="ts">
let { msg, msg2 } = defineModels<{
  msg: number;
  msg2: number;
}>();

const onClick = () => {
  [msg2.value, msg.value] = [msg.value, msg2.value];
};
</script>

<template>
  <button @click="onClick()">adsfsdf</button>
</template>
