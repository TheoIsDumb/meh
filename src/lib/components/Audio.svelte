<script>
  import Muted from "$lib/icons/Muted.svelte";
  import Unmuted from "$lib/icons/Unmuted.svelte";
  import Play from "$lib/icons/Play.svelte";

  let audio
  let muted = false
  let paused = false
</script>

<audio bind:this={audio} bind:paused bind:muted loop autoplay src="blippy.opus" />

<button on:click={() => muted = !muted }>
  {#if muted}
    <Muted />
  {:else}
    <Unmuted />
  {/if}
</button>

<button on:click={() => audio.play()}>
    <Play />
</button>

<style>
  button {
    border: 0;
    background-color: transparent;
    color: white;
  }
</style>