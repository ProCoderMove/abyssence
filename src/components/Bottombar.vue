<template>
  <footer
    class="p-4 m-4 rounded-lg bg-slate-600/30 backdrop-blur-md border border-slate-500/30 flex justify-between items-center"
  >
    <div class="flex items-center space-x-4">
      <span>Video View</span>
      <span>Pilot Gain: --%</span>
      <span>Lights: --%</span>
      <span>Cam Tilt: --%</span>
      <span>Depth: 0.00m</span>
      <span>Water Temp: --C</span>
    </div>
    <div class="flex items-center space-x-4">
      <span>Stream 1</span>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Bottombar",
};
</script>
