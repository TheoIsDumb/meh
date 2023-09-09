<script>
  import App from '$lib/components/App.svelte'
  import { parentDiv } from '$lib/store'
</script>

<div bind:this={$parentDiv}>
  <App />

</div>

<style>
  :global(body) { margin: 0; }

  div {
    width: 100dvw;
    height: 100dvh;
    background-color: #100113;
  }
</style>
