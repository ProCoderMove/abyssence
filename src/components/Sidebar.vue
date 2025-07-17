<template>
  <div
    class="w-64 p-4 m-4 rounded-lg bg-slate-600/30 backdrop-blur-md border border-slate-500/30"
  >
    <div class="flex items-center mb-8">
      <img src="../assets/logo.png" alt="Company Logo" class="w-10 h-10 mr-2" />
      <h1 class="text-xl font-bold">Abyssence</h1>
    </div>
    <nav>
      <ul>
        <li class="mb-4">
          <a
            href="#"
            class="flex items-center p-2 rounded-md hover:bg-slate-500/50"
          >
            <span class="mr-2">⌂</span>
            <span>Cockpit</span>
          </a>
        </li>
        <li class="mb-4">
          <a
            href="#"
            class="flex items-center p-2 rounded-md hover:bg-slate-500/50"
          >
            <span class="mr-2">📈</span>
            <span>Analytics</span>
          </a>
        </li>
        <li class="mb-4">
          <a
            href="#"
            class="flex items-center p-2 rounded-md hover:bg-slate-500/50"
          >
            <span class="mr-2">⚙</span>
            <span>Settings</span>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
};
</script>
