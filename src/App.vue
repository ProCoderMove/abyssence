<template>
  <div id="app" class="flex flex-col h-screen justify-between">
    <Topbar :title="topbar.title" :alert="topbar.alert" :time="topbar.time" />
    <div class="text-center">
      <p>{{ serverStatus }}</p>
      <p>{{ streamStatus }}</p>
    </div>
    <Bottombar
      :view="bottombar.view"
      :pilotGain="bottombar.pilotGain"
      :lights="bottombar.lights"
      :camTilt="bottombar.camTilt"
      :depth="bottombar.depth"
      :waterTemp="bottombar.waterTemp"
      :stream="bottombar.stream"
    />
  </div>
</template>

<script>
import Topbar from "./components/Topbar.vue";
import Bottombar from "./components/Bottombar.vue";

export default {
  name: "App",
  components: {
    Topbar,
    Bottombar,
  },
  data() {
    return {
      topbar: {
        title: "Finding Tidal Tranquility",
        alert: "No recent alerts.",
        time: new Date().toLocaleTimeString(),
      },
      bottombar: {
        view: "Video View",
        pilotGain: 0,
        lights: 0,
        camTilt: 0,
        depth: 0.0,
        waterTemp: 0,
        stream: "Stream 1",
      },
      serverStatus: "Server status: Signaller connection closed (14:44:41)",
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
