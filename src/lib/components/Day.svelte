<script>
    export let day;
</script>


<div class="day flex w-40 h-40 border-2 border-black rounded-xl hover:bg-lime-600 justify-end"> 
    <span class="day-text text-4xl mr-3 ">{day} </span>
</div>

<style>


.day:hover{
    color: white;
    cursor: pointer;
}

.day-text {
    font-weight: 700;
    font-family: 'Lobster', cursive;
    color: black;
}
</style>