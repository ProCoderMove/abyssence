<template>
  <footer
    class="p-4 bg-gray-800/30 backdrop-blur-md flex justify-between items-center"
  >
    <div class="flex items-center space-x-4">
      <span>{{ view }}</span>
      <span>Pilot Gain: {{ pilotGain }}%</span>
      <span>Lights: {{ lights }}%</span>
      <span>Cam Tilt: {{ camTilt }}%</span>
      <span>Depth: {{ depth }}m</span>
      <span>Water Temp: {{ waterTemp }}C</span>
    </div>
    <div class="flex items-center space-x-4">
      <span>{{ stream }}</span>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Bottombar",
  props: {
    view: String,
    pilotGain: Number,
    lights: Number,
    camTilt: Number,
    depth: Number,
    waterTemp: Number,
    stream: String,
  },
};
</script>
