<script>
  import Muted from "$lib/icons/Muted.svelte";
  import Unmuted from "$lib/icons/Unmuted.svelte";

  let muted = false
  let currentTime = 0
  let paused = false

  function repeat() {
    currentTime = 0
    paused = !paused
  }
</script>

<audio bind:paused bind:muted bind:currentTime on:ended={repeat} autoplay src="blippy.opus" />

<button on:click={() => muted = !muted }>
  {#if muted}
    <Muted />
  {:else}
    <Unmuted />
  {/if}
</button>

<style>
  button {
    border: 0;
    background-color: transparent;
    color: white;
  }
</style>