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

    :global(body.dark-mode .filter_white) {
      filter: invert(1) hue-rotate(180deg);
      
    }
    :root {
      --background: "#651515";
      --foreground: "#ffffff";

    }
</style>



<slot />