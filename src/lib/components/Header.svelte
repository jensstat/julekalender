<script>
    import Toggle from "./Toggle.svelte";
</script>

<div class="header flex justify-between items-center">
    <h1 class="">Jens' Adventskalender</h1>
    <h1 class="">Julen 2023</h1>
    <div class="toggle flex flex-row items-center gap-5"><h1 class="">Dark Mode</h1> <Toggle/></div>
</div>

<style>
.header {
    background-color: var(--background);
    height: 10vh;
    width: 100%;
}

h1 {
    font-size: 30px;
    font-family: 'Lobster', cursive;

    }
h2 {
    font-size: 25px;

    }
</style>