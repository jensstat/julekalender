<script>
import Header from "$lib/components/Header.svelte";
import Calendar from "$lib/components/Calendar.svelte";
import Icon from "$lib/assets/tree.svg"
let screenSize;


</script>


<svelte:window bind:innerWidth={screenSize} />
<div class="flex flex-col w-screen items-center">
    <div class="w-8/12">
        <Header />
    </div>

    <div class="flex flex-col md:flex-row md:self-center md:w-11/12 lg:items-center">
        {#if screenSize < 768}
        <img src="{Icon}" class="filter_white self-center h-32 mb-5" alt="tree">
        {:else}
        <img src="{Icon}" class="filter_white h-28 " alt="tree">
        {/if}
        <Calendar />
        {#if screenSize > 768}
        <img src="{Icon}" class="filter_white h-28" alt="tree">
        {/if}

    </div>  
</div>

<style>
    .filter_white{
        opacity: 0.5;
    }
</style>