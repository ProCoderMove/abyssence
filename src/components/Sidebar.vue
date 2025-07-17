<template>
  <div
    :class="[
      'bg-gray-800/30 backdrop-blur-md m-4 my-4 rounded-lg flex flex-col transition-all duration-300',
      isExpanded ? 'w-64' : 'w-20',
    ]"
  >
    <div class="flex items-center justify-center p-4">
      <button @click="toggle" class="p-2 rounded-md hover:bg-gray-700/50">
        <span v-if="isExpanded">&#9664;</span>
        <span v-else>&#9654;</span>
      </button>
    </div>
    <nav class="flex-1 px-4">
      <ul>
        <li class="mb-4">
          <a
            href="#"
            class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
          >
            <span class="text-2xl">🧭</span>
            <span v-if="isExpanded" class="ml-2">Compass</span>
          </a>
        </li>
        <li class="mb-4">
          <a
            href="#"
            class="flex items-center p-2 rounded-md hover:bg-gray-700/50"
          >
            <span class="text-2xl">🛰️</span>
            <span v-if="isExpanded" class="ml-2">GPS</span>
          </a>
        </li>
      </ul>
    </nav>
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
