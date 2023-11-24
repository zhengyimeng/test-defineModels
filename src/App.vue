<script setup lang="ts">
import { ref, watch } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

const msg = ref({ name: 123, label: 789 });
const msg2 = ref({ name: 65, label: 456 });

watch([msg, msg2], () => {
  console.log(1);
});

[msg.value, msg2.value] = [msg2.value, msg.value];
</script>

<template>
  <HelloWorld v-model:msg="msg" v-model:msg2="msg2" />
</template>
