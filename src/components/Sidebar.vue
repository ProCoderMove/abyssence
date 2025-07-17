<template>
  <div class="relative flex items-start pt-4">
    <div
      :class="[
        'bg-gray-800/30 backdrop-blur-md rounded-lg flex flex-col transition-all duration-300 ease-in-out',
        isExpanded ? 'w-64 p-4' : 'w-0 p-0',
      ]"
      class="h-[calc(100vh-2rem)] overflow-hidden"
    >
      <nav class="flex-1">
        <ul>
          <li class="mb-4">
            <a
              href="#"
              class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
            >
              <span class="text-2xl">✏️</span>
              <span v-if="isExpanded" class="ml-2">Edit Interface</span>
            </a>
          </li>
          <li class="mb-4">
            <a
              href="#"
              class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
            >
              <span class="text-2xl">📍</span>
              <span v-if="isExpanded" class="ml-2">Mission Planning</span>
            </a>
          </li>
          <li class="mb-4">
            <a
              href="#"
              class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
            >
              <span class="text-2xl">⚙️</span>
              <span v-if="isExpanded" class="ml-2">Settings</span>
            </a>
          </li>
          <li class="mb-4">
            <a
              href="#"
              class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
            >
              <span class="text-2xl">🖼️</span>
              <span v-if="isExpanded" class="ml-2">Enter Fullscreen</span>
            </a>
          </li>
          <li class="mb-4">
            <a
              href="#"
              class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
            >
              <span class="text-2xl">ℹ️</span>
              <span v-if="isExpanded" class="ml-2">About</span>
            </a>
          </li>
        </ul>
      </nav>
    </div>
    <button @click="toggle" class="p-2 rounded-md hover:bg-gray-700/50 ml-2">
      <span v-if="isExpanded">&#9664;</span>
      <span v-else>&#9654;</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      isExpanded: true,
    };
  },
  methods: {
    toggle() {
      this.isExpanded = !this.isExpanded;
    },
  },
};
</script>
