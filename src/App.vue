<template>
  <div class="relative flex h-screen bg-gray-900 text-white">
    <div id="app" class="flex-1 flex flex-col h-screen justify-between overflow-hidden">
      <Topbar
        :title="topbar.title"
        :alert="topbar.alert"
        :time="topbar.time"
        class="m-4"
      />
      <div class="relative flex-1 mx-4 mb-4">
        <div class="absolute inset-0 flex items-center justify-center">
          <div class="text-center">
            <p>{{ serverStatus }}</p>
            <p>{{ streamStatus }}</p>
          </div>
        </div>
        <Sidebar />
      </div>
      <Bottombar class="m-4" />
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
