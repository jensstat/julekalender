<script>
    import "../app.css";

</script>
  
<style>
    :global(body) {
      background-color: white;
      display: flex;
      color: black;
      justify-content: center;
      font-family: 'Lobster', cursive;
      transition: background-color 0.3s

    }
    :global(body.dark-mode){
      background: #651515;
      color: white;
    }
    

    :root {
      --background: "#651515";
      --foreground: "#ffffff";

    }
</style>



<slot />