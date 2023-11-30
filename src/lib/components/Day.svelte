<script>
    export let day;
</script>


<div class="day dark:bg-white flex w-40 h-40 border-2 border-black rounded-xl hover:bg-lime-600 justify-end"> 
    <span class="day-text text-4xl mr-3 ">{day} </span>
</div>

<style>

.day:hover{
    background-color: rgb(101 163 13 / var(--tw-bg-opacity));
    cursor: pointer;
}
.day-text {
    font-weight: 700;
    font-family: 'Lobster', cursive;
    color: black;
}
</style>