<script>
    import Day from "./Day.svelte";
    let days = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24];
    const quotes = [
  "Why was the snowman looking through the carrots? He was picking his nose!",
  "What do you get if you cross a snowman and a vampire? Frostbite!",
  "What do you call an elf who sings? A wrapper!",
  "Why did Santa go to music school? To improve his wrapping skills!",
  "What do you call Santa when he takes a break? Santa Pause!",
  "How does Santa keep his suit wrinkle-free? He uses Claus-tarch!",
  "Why did the Christmas tree go to the barber? It needed a trim!",
  "What do you get if you cross a snowman and a dog? Frostbite!",
  "How do you know if Santa is a good race car driver? He always wraps his sled around the pole!",
  "What do you call Santa when he takes a break? Santa Paws!",
  "Why was the math book sad at Christmas? Because it had too many 'problems'!",
  "What do you get if you cross a snowman and a dog? Frosty Paws!",
  "What did one snowman say to the other? 'Do you smell carrots?'",
  "Why did the Christmas cookie go to the doctor? It was feeling crumbly!",
  "How do you know when Santa's in the room? You can sense his presents!",
  "What do you get if you cross a snowman and a vampire? Frostbite!",
  "Why did the turkey join the band? Because it had the drumsticks!",
  "What's Santa's favorite pizza? One that's deep-pan, crisp, and even!",
  "What do you call Santa when he loses his pants? Saint Knickerless!",
  "Why was the snowman looking through the carrots? He was picking his nose!",
  "What do you call Santa when he takes a break? Santa Pause!",
  "What do you get if you cross a snowman and a dog? Frostbite!",
  "How does Santa keep his suit wrinkle-free? He uses Claus-tarch!",
  "What did Santa say to the smoker? Please don't smoke, it's bad for my elf!"
];

    let currentDay = 0;
</script>

<div class="calendar flex md:w-11/12 justify-center flex-wrap gap-2">
{#if currentDay == 0}
{#each days as day}
<div on:click={() => {currentDay = day; console.log(currentDay)}}>
    <Day day={day} />

</div>
{/each}
{/if}

{#if currentDay != 0}
<div class="quotepage w-full flex flex-col items-center md:block">
    <button class="back-button mt-5 mb-5 md:mt-0 md:mb-0" on:click={() => {
        currentDay = 0;
    }}><span>Tilbake</span></button>
    <div class="flex items-center "> 
        <div class="quote flex  dark:text-white">
            <span class="quote_text text-4xl md:text-8xl/loose">{quotes[currentDay]}</span>
        </div>
    </div>
</div>
{/if}
</div>
<style>
    .back-button {
        background: darkgreen;
        color: white;
        width: 200px;
        padding: 5px 10px;
        border-radius: 10px;
    }
    

    .quote_text{
        text-align: center;
    }

    

</style>