<script>
    import Header from "$lib/components/Header.svelte";
    import Calendar from "$lib/components/Calendar.svelte";
    import Icon from "$lib/assets/tree.svg";
    
    let screenSize;
  </script>
  
  <svelte:window bind:innerWidth={screenSize} />
  
  <div class="flex flex-col min-h-screen items-center pt-5 md:pt-0">
    <div class="w-8/12">
      <Header />
    </div>
  
    <div class="flex flex-col md:flex-row md:w-11/12 items-center">
      {#if screenSize < 768}
        <img src="{Icon}" class="filter_white self-center h-32 mb-5 dark:invert dark:hue-rotate-180" alt="tree" />
      {:else}
        <img src="{Icon}" class="filter_white h-32 dark:invert dark:hue-rotate-180" alt="tree" />
      {/if}
  
      <Calendar />
  
      {#if screenSize > 768}
        <img src="{Icon}" class="filter_white h-28 dark:invert dark:hue-rotate-180" alt="tree" />
      {/if}
  
      {#if screenSize < 768}
        <img src="{Icon}" class="filter_white self-center mt-12 h-32 mb-5 dark:invert dark:hue-rotate-180" alt="tree" />
      {/if}
    </div>
  </div>
  
  <style>
    .filter_white {
      opacity: 0.5;
    }
  </style>
  