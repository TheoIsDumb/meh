<script>
    import { color } from '$lib/store'

    let colors = ['#fc0a46', '#049ef4', '#c9e0de']
</script>

<div class="buttons">
    {#each colors as c}
        <button style="background-color: {c}"
            on:click={() => $color = c}
        />
    {/each}
</div>

<style>
    div.buttons {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
    }
    button {
        all: unset;
        height: 2rem;
        width: 2rem;
        border-radius: 50%;
        border: 3px solid black;
    }
</style>