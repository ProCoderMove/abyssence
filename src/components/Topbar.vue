<template>
  <div
    class="w-full backdrop-blur-xl bg-white/50 border border-white/30 shadow-lg rounded-xl p-4 flex justify-between items-center"
  >
    <div class="text-sm text-gray-700">
      <span class="font-medium">Status:</span>
      <span class="text-green-600 font-semibold">Connected</span>
    </div>
    <div class="text-sm text-gray-700">
      {{ currentTime }}
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const currentTime = ref(new Date().toLocaleTimeString());

onMounted(() => {
  setInterval(() => {
    currentTime.value = new Date().toLocaleTimeString();
  }, 1000);
});
</script>
