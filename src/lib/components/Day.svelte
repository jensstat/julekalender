<script>
    export let day;
</script>


<div class="day">
    <span class="day-text">{day} </span>
</div>

<style>
.day {
    display: flex;
    width: 165px;
    height: 165px;
    border: 1px solid black;
    background-color: white;
    border-radius: 10px;
    justify-content: flex-end;
}

.day:hover{
    background-color: darkgreen;
    color: white;
    cursor: pointer;
}

.day-text {
    margin-right: 20px;
    font-size: 40px;
    font-weight: 700;
    font-family: 'Lobster', cursive;
    color: black;
}
</style>