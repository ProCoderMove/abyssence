<template>
  <div class="flex h-screen bg-gray-900 text-white">
    <Sidebar />
    <div id="app" class="flex-1 flex flex-col h-screen justify-between overflow-hidden">
      <Topbar
        :title="topbar.title"
        :alert="topbar.alert"
        :time="topbar.time"
        class="mx-4 mt-4"
      />
      <div class="text-center flex-1">
        <p>{{ serverStatus }}</p>
        <p>{{ streamStatus }}</p>
      </div>
      <Bottombar class="mx-4 mb-4" />
    </div>
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar.vue";
import Topbar from "./components/Topbar.vue";
import Bottombar from "./components/Bottombar.vue";

export default {
  name: "App",
  components: {
    Sidebar,
    Topbar,
    Bottombar,
  },
  data() {
    return {
      topbar: {
        title: "Solving the Nautical Enigma",
        alert: "No recent alerts.",
        time: new Date().toLocaleTimeString(),
      },
      serverStatus: "Server status: Reconnecting to signalling (15:58:22)",
      streamStatus: "Stream status: waiting...",
    };
  },
  mounted() {
    setInterval(() => {
      this.topbar.time = new Date().toLocaleTimeString();
    }, 1000);
  },
};
</script>
