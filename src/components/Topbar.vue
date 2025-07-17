<template>
  <header
    class="p-4 mx-4 mt-4 rounded-lg bg-gray-800/30 backdrop-blur-md flex justify-between items-center"
  >
    <h1 class="text-xl">{{ title }}</h1>
    <div class="flex items-center space-x-4">
      <span>{{ alert }}</span>
      <span>{{ time }}</span>
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
