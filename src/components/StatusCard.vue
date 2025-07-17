<template>
  <div
    class="backdrop-blur-xl bg-white/60 border border-white/30 rounded-xl p-4 shadow-md"
  >
    <div class="flex items-center gap-3">
      <div class="text-2xl">{{ icon }}</div>
      <div>
        <div class="text-sm text-gray-600">{{ label }}</div>
        <div class="text-xl font-bold text-[#004AA4]">
          {{ value }} <span class="text-sm text-gray-500">{{ unit }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  label: String,
  value: [String, Number],
  unit: {
    type: String,
    default: "",
  },
  icon: {
    type: String,
    default: "❔",
  },
});
</script>
