<script>
  import Muted from "$lib/icons/Muted.svelte";
  import Unmuted from "$lib/icons/Unmuted.svelte";

  let muted = false
  let paused = false

  $: console.log(paused)
</script>

<audio bind:paused bind:muted loop autoplay src="blippy.opus" />

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