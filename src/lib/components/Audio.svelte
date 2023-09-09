<script>
  import Muted from "$lib/icons/Muted.svelte"
  import Unmuted from "$lib/icons/Unmuted.svelte"
  import Play from "$lib/icons/Play.svelte"

  let audio
  let muted = false
</script>

<audio bind:this={audio} bind:muted loop autoplay src="blippy.opus" />

<button class="empty" on:click={() => muted = !muted }>
  {#if muted}
    <Muted />
  {:else}
    <Unmuted />
  {/if}
</button>

<button class="empty" on:click={() => audio.play()}>
    <Play />
</button>