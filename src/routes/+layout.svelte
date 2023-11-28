<script>
    import "../app.css";

</script>
  
<style>
    :global(body) {
      font-family: 'Lobster', cursive;
      transition: background-color 0.5s;
    }
    :root {
      --background: "#651515";
      --foreground: "#ffffff";
    }

    :global(body.dark){
      background-color: rgb(153 27 27 / 1);
    }

</style>



<slot />