<template>
  <div id="app" class="flex flex-col h-screen">
    <Topbar />
    <main class="flex-1 p-4">
      <Dashboard />
    </main>
    <Bottombar />
  </div>
</template>

<script>
import Topbar from "./components/Topbar.vue";
import Bottombar from "./components/Bottombar.vue";
import Dashboard from "./components/Dashboard.vue";

export default {
  name: "App",
  components: {
    Topbar,
    Bottombar,
    Dashboard,
  },
};
</script>
