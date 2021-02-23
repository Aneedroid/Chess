<script>
    export let colorIndex;

    const squareClass = (colorIndex) => {
        let color;
        const row = Math.floor(colorIndex/8);

        if(row % 2 == 0) {
            // Starts with lite.
            if((colorIndex % 2) == 0) color = 'lite';
            else color = 'dark';
        }
        else {
            if((colorIndex % 2) == 0) color = 'dark';
            else color = 'lite';
        }
        return color;
    };
</script>

<style>
    div {
        height: 4rem;
        width: 4rem;
        background-color: hotpink;
    }

    .lite {
        background-color: #F5DEB3;
    }

    .dark {
        background-color: #8B4513;
    }
</style>

<div class={squareClass(colorIndex)}>{colorIndex}</div>