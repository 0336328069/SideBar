<script>
// @ts-nocheck

  import IconButton from "./IconButton.svelte";
  export let sideBarList = [];
</script>

<div class="sidebar">
    {#each sideBarList as item}
        <div class="relative sidebar-item">
            <div class={`active-custom`}></div>
            <IconButton icon={item} />
        </div>
    {/each}
</div>

<style lang="scss">
  .sidebar {
    @apply w-[5.5rem] min-w-[5.5rem] h-screen bg-[#1E1F22] flex flex-col items-center gap-3 pt-5;

    .sidebar-item{
        .active-custom {
            @apply absolute w-[10px] rounded-r-md -ml-1 h-2 top-[25px] -left-4 bg-white transition-all duration-200 ease-in-out;
        }

        .sidebar-active{
            @apply top-0 h-full;
        }
        
        &:hover{
            .active-custom{
                @apply h-[24px] top-[16px];
            }
        }
    }
  }
</style>
