<script>
    import Toggle from "./Toggle.svelte";
    const audioFilePath = "/song.mp3"; // Update with your actual file path

    const playSong = () => {
        const audio = new Audio(audioFilePath);
        audio.autoplay = true;
    };
</script>

<div class="header">
    <div class="flex flex-col justify-around gap-3 md:p-7 md:flex-row md:justify-between items-center text-center dark:text-white">
        <span class="text-3xl  md:text-3xl"><div>
            <button on:click={playSong}>Jens' Adventskalender</button>
          </div></span>
        <span class="text-2xl md:text-3xl">Julen 2023</span>
        <div class="toggle flex flex-row items-center gap-5"><span class="text-xl md:text-3xl">Dark Mode</span> <Toggle/>
        </div>
    </div>
</div>

<style>


h1 {
    font-family: 'Lobster', cursive;

    }

</style>