<script>
    import Square from './Square.svelte';
</script>

<style>
    .ground {
        display: flex;
        background-color: tomato;
        height: 45rem;
        width: 60rem;
        margin: auto;
    }

    .board {
        display: flex;
        margin: 2rem;
        background-color: green;
        height: 32rem;
        width: 32rem;
        margin: auto;
        flex-wrap: wrap;
    }

</style>

<div class="ground">
    <div class="board">
        {#each Array(64) as _, i}
            <Square colorIndex={i} />
        {/each}
    </div>
</div>