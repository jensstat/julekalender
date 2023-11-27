<script>
    import Day from "./Day.svelte";
    let days = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24];
    let quotes = [
  "Hvorfor kan ikke sykler stå av seg selv? Fordi de er tohjulede!",
  "Hva sa den ene veggen til den andre veggen? Jeg støtter deg!",
  "Hvorfor kan ikke duoen bestemme seg? Fordi de er uenige!",
  "Hva er et smil? Det er en lyd som en nøkkelring gjør når den kastes i søppelbøtten!",
  "Hvorfor var fotballspilleren så god på matematikk? Fordi han alltid scoret i tillegg!",
  "Hvorfor kan ikke duoen bestemme seg? Fordi de er uenige!",
  "Hva gjorde den ene veggtenen til den andre vekten? Jeg tror du veier for mye!",
  "Hvorfor var fiskens skole så dårlig? Fordi den var fylt med nulldykker!",
  "Hva sa den ene poteten til den andre? Jeg liker deg!",
  "Hvorfor kunne ikke sykkelen stå oppreist av seg selv? Fordi den var to-tung!",
  "Hva kaller man en gruppe med musikalske hvaler? En orkesterskval!",
  "Hvorfor spilte ikke skjelettene på musikk? Fordi de ikke hadde motet!",
  "Hva sa den ene geita til den andre? Hva har du gjort, geit det til meg!",
  "Hvorfor kan ikke nesen din være 12 tommer lang? Fordi det ville være en fot!",
  "Hvorfor kan ikke duoen bestemme seg? Fordi de er uenige!",
  "Hva sa den ene gulroten til den andre? Du er fantastisk!",
  "Hvorfor har ikke telefonen hatt noen venner? Fordi den alltid er opptatt!",
  "Hva gjør du hvis du ser en banan på gulvet? Du tråkker på den!",
  "Hvorfor tok ikke sykkelen eksamen? Fordi den var to-tung!",
  "Hva sa det ene eplet til det andre? Jeg har eplefølelser for deg!",
  "Hvorfor var blyanten trøtt? Fordi den hadde alltid blytunge dager!",
  "Hva sa den ene ketchupen til den andre? Ketch-up!",
  "Hvorfor var det stille i biblioteket? Fordi alle bøkene var ute!",
  "Hva sa den ene foten til den andre? Du er tråkket på min tå!",
  "Hvorfor kan ikke duoen bestemme seg? Fordi de er uenige!",
  "Hva sa det ene treet til det andre? Jeg savner deg allerede!",
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
<div class="quotepage w-full">
    <button class="back-button" on:click={() => {
        currentDay = 0;
    }}><span>Tilbake</span></button>
    <div class="quote flex justify-center items-center mt-48">
        <span class="quote_text text-4xl md:text-8xl/loose">{quotes[currentDay]}</span>
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