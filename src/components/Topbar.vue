<template>
  <header
    class="p-4 m-4 mb-0 rounded-lg bg-slate-600/30 backdrop-blur-md border border-slate-500/30 flex justify-between items-center"
  >
    <h1 class="text-xl">Finding Tidal Tranquility</h1>
    <div class="flex items-center space-x-4">
      <span>No recent alerts.</span>
      <span>{{ currentTime }}</span>
    </div>
  </header>
</template>

<script>
export default {
  name: "Topbar",
  data() {
    return {
      currentTime: new Date().toLocaleTimeString(),
    };
  },
  mounted() {
    setInterval(() => {
      this.currentTime = new Date().toLocaleTimeString();
    }, 1000);
  },
};
</script>
