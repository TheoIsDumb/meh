<script>
  import Audio from './Audio.svelte';
  import ColorPalette from './ColorPalette.svelte';
</script>

<div class="sidebar">
  <ColorPalette />
  <Audio />
</div>

<style>
  div.sidebar {
    position: fixed;
    bottom: 1rem;
    right: 1rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
</style>