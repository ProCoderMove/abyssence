<template>
  <header
    class="p-4 bg-gray-800/20 backdrop-blur-lg border border-white/10 shadow-lg rounded-lg flex justify-between items-center"
  >
    <h1 class="text-xl font-light">{{ title }}</h1>
    <div class="flex items-center space-x-4">
      <span class="text-sm font-light">{{ alert }}</span>
      <span class="text-sm font-light">{{ time }}</span>
    </div>
  </header>
</template>

<script>
export default {
  name: "Topbar",
  props: {
    title: String,
    alert: String,
    time: String,
  },
};
</script>
