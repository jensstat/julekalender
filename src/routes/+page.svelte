<script>
import Header from "$lib/components/Header.svelte";
import Calendar from "$lib/components/Calendar.svelte";
import Icon from "$lib/assets/tree.svg"


</script>

<div class="flex flex-col w-screen justify-center">
    <div class="w-8/12 self-center">
        <Header />
    </div>
    <div class="flex flex-row self-center w-screen">
        <img src="{Icon}" class="filter_white w-2/12" alt="tree">
        <Calendar />
        <img src="{Icon}" class="filter_white w-2/12" alt="tree">
    </div>  

</div>
