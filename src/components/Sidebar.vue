<template>
  <div>
    <!-- Toggle Button -->
    <button
      @click="toggle"
      :class="[
        'absolute top-1/2 -translate-y-1/2 p-2 rounded-full bg-gray-800/50 hover:bg-gray-700/80 z-20 transition-all duration-300 ease-in-out',
        isExpanded ? 'left-64' : 'left-0',
      ]"
    >
      <span v-if="isExpanded" class="text-white">&#9664;</span>
      <span v-else class="text-white">&#9654;</span>
    </button>

    <!-- Sidebar Panel -->
    <div
      :class="[
        'absolute top-0 left-0 h-full bg-gray-800/20 backdrop-blur-lg border border-white/10 shadow-lg rounded-lg transition-all duration-300 ease-in-out z-10',
        isExpanded ? 'w-64 p-4' : 'w-0 p-0 opacity-0',
      ]"
      class="overflow-hidden"
    >
      <div v-if="isExpanded" class="h-full flex flex-col">
        <nav class="flex-1 mt-10">
          <ul>
            <li class="mb-4">
              <a
                href="#"
                class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
              >
                <span class="text-2xl">✏️</span>
                <span class="ml-2">Edit Interface</span>
              </a>
            </li>
            <li class="mb-4">
              <a
                href="#"
                class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
              >
                <span class="text-2xl">📍</span>
                <span class="ml-2">Mission Planning</span>
              </a>
            </li>
            <li class="mb-4">
              <a
                href="#"
                class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
              >
                <span class="text-2xl">⚙️</span>
                <span class="ml-2">Settings</span>
              </a>
            </li>
            <li class="mb-4">
              <a
                href="#"
                class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
              >
                <span class="text-2xl">🖼️</span>
                <span class="ml-2">Enter Fullscreen</span>
              </a>
            </li>
            <li class="mb-4">
              <a
                href="#"
                class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
              >
                <span class="text-2xl">ℹ️</span>
                <span class="ml-2">About</span>
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  data() {
    return {
      isExpanded: false,
    };
  },
  methods: {
    toggle() {
      this.isExpanded = !this.isExpanded;
    },
  },
};
</script>
