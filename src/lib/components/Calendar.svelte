<script>
    import Day from "./Day.svelte";
    let days = [1,2,3];
</script>

<div class="calendar">
<Day day = {1}/>
<!-- {#each days as day}
    <Day day={day}/>
{/each} -->

</div>
<style>

</style>