<script>
  import SideBar from "./lib/components/SideBar.svelte";
  const sideBarList = [
    'icon-filled-logo-color-instagram',
    'icon-filled-logo-color-linkedin',
    'icon-filled-logo-color-tiktok',
    'icon-filled-logo-color-telegram'
  ]
</script>

<main>
  <div class="w-full h-full flex">
    <SideBar sideBarList={sideBarList} />
    <div class="bg-[#313338] w-full">
      <!-- // Body -->
    </div>
  </div>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
