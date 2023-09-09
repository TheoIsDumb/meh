<script>
  import { browser } from '$app/environment'
  import { parentDiv } from '$lib/store'
  import FullScreenIcon from '$lib/icons/FullScreenIcon.svelte'
  import FullScreenExit from '$lib/icons/FullScreenExit.svelte'

  let openFullscreen

  if (browser) {
    openFullscreen = () => {
        if (!document.fullscreenElement) {
        $parentDiv.requestFullscreen()
        } else {
        document.exitFullscreen()
        }
    }
}
</script>

<button class="empty" on:click={openFullscreen}>
    {#if browser}
        {#if document.fullscreenElement}
            <FullScreenExit />
        {:else}
            <FullScreenIcon />
        {/if}
    {/if}
</button>