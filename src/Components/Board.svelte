<script>
    import Square from './Square.svelte';
</script>

<style>
    .ground {
        display: flex;
        height: 45rem;
        flex-direction: column;
        align-items: center;
    }

    .board {
        display: flex;
        margin: 2rem;
        background-color: green;
        height: 32rem;
        width: 32rem;
        flex-wrap: wrap;
        box-shadow: rgba(0, 0, 0, 0.7) 0px 19px 38px, rgba(0, 0, 0, 0.1) 0px 15px 12px;
    }

    .middle {
        display: flex;
        margin: 2rem;
        justify-content: center;
    }

    .grid-top {
        display: flex;
        justify-content: center;
        transform: translate(0rem , 1rem);
        width: 32rem;
    }

    .grid-middle-left {
        display: flex;
        flex-wrap: wrap;
        width: 0rem;
        transform: translate(-2rem, 2rem);
        height: 32rem;
    }

    .x-coordinate {
        display: flex;
        justify-content: center;
        width: 4rem;
        font-style: italic;
        font-weight: 600;
    }

    .y-coordinate {
        display: flex;
        flex-direction: column;
        justify-content: center;
        font-style: italic;
        font-weight: 600;
    }

</style>

<div class="ground">
    <div class="grid-top">
        {#each ['a','b','c','d','e','f','g','h'] as xCoordi}
            <div class="x-coordinate">{xCoordi}</div>
        {/each}
    </div>
    <div class="middle">
        <div class="grid-middle-left">
            {#each Array(8) as _,yCoordi}
                <div class="y-coordinate">{yCoordi + 1}</div>
            {/each}
        </div>
        <div class="board">
            {#each Array(64) as _, i}
                <Square colorIndex={i} />
            {/each}
        </div>
    </div>
</div>