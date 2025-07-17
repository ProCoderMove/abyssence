<template>
  <div id="app" class="flex h-screen">
    <Sidebar />
    <div class="flex-1 flex flex-col">
      <Topbar />
      <main class="flex-1 p-4">
        <Dashboard />
      </main>
    </div>
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar.vue";
import Topbar from "./components/Topbar.vue";
import Dashboard from "./components/Dashboard.vue";

export default {
  name: "App",
  components: {
    Sidebar,
    Topbar,
    Dashboard,
  },
};
</script>
