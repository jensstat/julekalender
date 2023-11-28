<script>
    let click = false
    let darkMode = false

    import { writable } from "svelte/store";
    export const theme = writable(false);

    function clicker() {
        click = !click
        document.body.classList.toggle("dark")
    }

</script>


<button on:click={clicker} class="toggle">
    {#if click}
        <i class="indicator_move"></i>
    {:else}
        <i class="indicator"></i>
    {/if}

</button>
<style>
    .toggle {
        position: relative ;
        display: block;
        width: 80px;
        height: 40px;
        border-radius: 40px;
        background: #222;
        cursor: pointer;
        box-shadow: 0 8px 60px rgba(0,0,0,0.1),
                    inset 0 8px 8px rgba(0,0,0,0.1),
                    inset 0 -4px 4px rgba(0,0,0,0.1);
    }

    .toggle .indicator {
        position: absolute;
        top: 0;
        left: 0;
        width: 40px;
        height: 40px;
        background: linear-gradient(to bottom, #444, #222);
        border-radius: 50%;
        transform: scale(0.9);
        box-shadow: 0 8px 40px rgba(0,0,0,0.5),
                    inset 0 4px 4px rgba(255,255,255,0.2),
                    inset 0 4px 4px rgba(0,0,0,0.1);
        transition: 0.5s;
    }

    .indicator_move {
        position: absolute;
        top: 0;
        left: 50;
        width: 40px;
        height: 40px;
        background: linear-gradient(to bottom, #444, #222);
        border-radius: 50%;
        transform: scale(0.9);
        box-shadow: 0 8px 40px rgba(0,0,0,0.5),
                    inset 0 4px 4px rgba(255,255,255,0.2),
                    inset 0 4px 4px rgba(0,0,0,0.1);
        transition: 0.5s;
    }
    
</style>
