<script>
  export let icon;
  export let isActive;
  const urlImg = import.meta.env.VITE_URL_IMG;
</script>

<div class={`icon-button ${isActive ? "isActive" : ""}`}>
  <img src={`${urlImg}/icons/${icon}.svg`} alt={icon} height="26" width="26" />
  <div class="tooltip">{icon} Icon</div>
</div>

<style lang="scss">
  .icon-button {
    @apply w-[60px] h-[60px] gap-y-3 flex justify-center items-center mx-auto bg-[#23272a] rounded-full hover:rounded-2xl hover:bg-green-500 cursor-pointer transition-all duration-100 ease-in-out;

    .tooltip {
      @apply invisible opacity-0 bg-black max-w-[300px] min-w-[300px] text-white items-center p-2 rounded-md absolute z-[1] top-[14px] left-[120px] -ml-[30px] transition-opacity duration-500 ease-in-out;
    }

    &.isActive {
      @apply bg-green-500 rounded-2xl;
    }

    &:hover {
      .tooltip {
        @apply visible opacity-100;
      }
    }
  }
</style>
