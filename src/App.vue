<template>
  <div class="min-h-screen flex flex-col md:flex-row p-4 gap-4">
    <Sidebar />
    <div class="flex-1 flex flex-col gap-4">
      <TopBar />
      <Dashboard />
    </div>
  </div>
</template>

<script setup>
import Sidebar from "./components/Sidebar.vue";
import TopBar from "./components/TopBar.vue";
import Dashboard from "./components/Dashboard.vue";
</script>
