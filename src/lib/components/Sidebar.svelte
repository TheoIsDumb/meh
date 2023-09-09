<script>
  import Audio from './Audio.svelte'
  import ColorPalette from './ColorPalette.svelte'
  import Github from '$lib/icons/Github.svelte'
  import Fullscreen from './Fullscreen.svelte'
</script>

<div class="sidebar">
  <ColorPalette />
  <Audio />

  <Fullscreen />

  <a href="https://github.com/theoisdumb/meh" target="_blank" noopener noreferrer>
    <Github />
  </a>
</div>

<style>
  div.sidebar {
    position: fixed;
    bottom: 1rem;
    right: 1rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: center;
  }
  :global(button.empty) {
    border: 0;
    background-color: transparent;
    color: white;
  }
</style>