<script>
    import "../app.css";

</script>
  
<style>
    :global(body) {
      background-color: #f2eee2;
      display: flex;
      justify-content: center;
      font-family: "Roboto", sans-serif;
      transition: background-color 0.3s

    }
    :global(body.dark-mode){
      background: #651515;
    }
    :root {
      --background: "#651515";
      --foreground: "#ffffff";

    }
</style>



<slot />