<template>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
    <StatusCard label="Battery" :value="battery" unit="%" icon="🔋" />
    <StatusCard label="Controller" :value="controller" unit="%" icon="🎮" />
    <StatusCard label="Alerts" :value="alertCount" icon="⚠️" />
  </div>
</template>

<script setup>
import StatusCard from "./StatusCard.vue";
import { ref } from "vue";

const battery = ref(87);
const controller = ref(98);
const alertCount = ref(2);
</script>
