<script>
    import Day from "./Day.svelte";
    let days = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24];
    let quotes = [
    " ",
    "Why don't scientists trust atoms? Because they make up everything!",
    "Did you hear about the mathematician who’s afraid of negative numbers? He'll stop at nothing to avoid them!",
    "I only know 25 letters of the alphabet. I don't know y.",
    "I only know 25 letters of the alphabet. I don't know y.",
    "Why don't skeletons fight each other? They don't have the guts.",
    "Why did the scarecrow win an award? Because he was outstanding in his field!",
    "How does a penguin build its house? Igloos it together!",
    "What do you call fake spaghetti? An impasta!",
    "Why did the coffee file a police report? It got mugged!",
    "I told my wife she should embrace her mistakes. She gave me a hug.",
    "What do you call a fish wearing a crown? A kingfish!",
    "How does a penguin build its house? Igloos it together!",
    "Why don't seagulls fly over the bay? Because then they'd be bagels!",
    "I only know 25 letters of the alphabet. I don't know y.",
    "Why did the bicycle fall over? Because it was two-tired!",
    "I told my wife she should embrace her mistakes. She gave me a hug.",
    "Why did the scarecrow win an award? Because he was outstanding in his field!",
    "Parallel lines have so much in common. It’s a shame they’ll never meet.",
    "Why don't skeletons fight each other? They don't have the guts.",
    "What do you call a fish wearing a crown? A kingfish!",
    "Why did the coffee file a police report? It got mugged!",
    "What do you call fake spaghetti? An impasta!",
    "Did you hear about the mathematician who’s afraid of negative numbers? He'll stop at nothing to avoid them!",
]

    let currentDay = 0;
</script>

<div class="calendar">
{#if currentDay == 0}
{#each days as day}
<div on:click={() => {currentDay = day; console.log(currentDay)}}>
    <Day day={day} />

</div>
{/each}
{/if}

{#if currentDay != 0}
<div class="quotepage w-full">
    <button class="back-button" on:click={() => {
        currentDay = 0;
    }}><span>Tilbake</span></button>
    <div class="quote grid flex-col">
        <span class="quote_text">{quotes[currentDay]}</span>
    </div>
    
</div>
{/if}
</div>
<style>
    
    .calendar {
        display: flex;
        height: 80vh;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    .back-button {
        background: darkgreen;
        color: white;
        width: 200px;
        padding: 5px 10px;
        border-radius: 10px;
    }
    
    .quote {
        margin-top: -5vh;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;    
    }

    .quote_text{
        font-size: 80px;
        text-align: center;
    }

    

</style>