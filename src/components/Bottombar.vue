<template>
  <footer
    class="p-4 bg-gray-800/20 backdrop-blur-lg border border-white/10 shadow-lg rounded-lg flex justify-between items-center"
  >
    <div class="flex items-center space-x-4">
      <div class="relative">
        <button
          @click="toggleDropdown"
          class="flex items-center space-x-2 p-2 rounded-md hover:bg-gray-700/50"
        >
          <span class="font-light">{{ selectedView }}</span>
          <span class="font-light">&#9662;</span>
        </button>
        <div
          v-if="isDropdownOpen"
          class="absolute bottom-full mb-2 w-48 bg-gray-800/80 rounded-md"
        >
          <ul>
            <li
              v-for="view in views"
              :key="view"
              @click="selectView(view)"
              class="p-2 hover:bg-gray-700/50 cursor-pointer font-light"
            >
              {{ view }}
            </li>
          </ul>
        </div>
      </div>
      <div class="flex items-center space-x-2">
        <span class="text-2xl">👷</span>
        <span class="font-light">--% Pilot Gain</span>
      </div>
      <div class="flex items-center space-x-2">
        <span class="text-2xl">🔦</span>
        <span class="font-light">--% Lights (1)</span>
      </div>
      <div class="flex items-center space-x-2">
        <span class="text-2xl">📷</span>
        <span class="font-light">--% Cam Tilt</span>
      </div>
      <div class="flex items-center space-x-2">
        <span class="text-2xl">🌊</span>
        <span class="font-light">0.00m Depth</span>
      </div>
      <div class="flex items-center space-x-2">
        <span class="text-2xl">🌡️</span>
        <span class="font-light">--C Water Temp</span>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Bottombar",
  data() {
    return {
      isDropdownOpen: false,
      selectedView: "Video View",
      views: ["Video View", "Map View", "Data View"],
    };
  },
  methods: {
    toggleDropdown() {
      this.isDropdownOpen = !this.isDropdownOpen;
    },
    selectView(view) {
      this.selectedView = view;
      this.isDropdownOpen = false;
    },
  },
};
</script>
