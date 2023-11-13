<script>
    import Toggle from "./Toggle.svelte";
</script>

<div class="header grid grid-cols-3 gap-4 place-items-center">
    <h1 class="justify-self-start ">Jens Adventskalender</h1>
    <h2 class="justify-self-end">Julen 2023</h2>
    <Toggle/>
</div>

<style>
.header {
    background-color: var(--background);
    height: 10vh;
    width: 100%;
}

h1 {
    color: #fff;
    font-size: 30px;
    font-family: 'Lobster', cursive;

    }
h2 {
    color: #B2B2B2;
    font-size: 25px;

    }
</style>