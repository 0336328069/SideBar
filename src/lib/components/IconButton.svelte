<script>
  export let icon;
  const urlImg = import.meta.env.VITE_URL_IMG;
</script>

<div class='icon-button'>
  <img class="img-filter" src={`${urlImg}/icons/${icon}.svg`} alt={icon} height="26" width="26" />
  <div class="tooltip">{icon} Icon</div>
</div>

<style lang="scss">
  .icon-button {
    @apply w-[60px] h-[60px] gap-y-3 flex justify-center items-center mx-auto bg-[#313338] rounded-full hover:rounded-2xl hover:bg-[#23a559] cursor-pointer transition-all duration-100 ease-in-out;

    .tooltip {
      @apply invisible opacity-0 bg-black max-w-[300px] min-w-[300px] text-white items-center p-2 rounded-md absolute z-[1] top-[14px] left-[120px] -ml-[30px] transition-opacity duration-500 ease-in-out;
    }

    &.isActive {
      @apply bg-green-500 rounded-2xl;

      
      .img-filter{
        filter: brightness(0) saturate(100%) invert(97%) sepia(99%) saturate(2%) hue-rotate(248deg) brightness(118%) contrast(100%) !important;
      }
    }

    &:hover {
      .tooltip {
        @apply visible opacity-100;
      }

      .img-filter{
        filter: brightness(0) saturate(100%) invert(97%) sepia(99%) saturate(2%) hue-rotate(248deg) brightness(118%) contrast(100%) !important;
      }
    }

    .img-filter{
      filter: brightness(0) saturate(100%) invert(51%) sepia(55%) saturate(652%) hue-rotate(92deg) brightness(92%) contrast(80%);
    }
  }
</style>
