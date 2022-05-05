<script>
  import Map from './lib/map.svelte';

  let showMap = false;
  function toggleMap() {
    if(showMap) {
      showMap = false;
    } else {
      showMap = true;
    }
    
  }
</script>

<main>
  <h1>Hello Map</h1>
  <label>
    <input type="checkbox" bind:checked={showMap}>
    Show Map
  </label>
  
  <button on:click={() => {toggleMap()}}>Show The Map</button>

{#if showMap}
  <div id="mapdiv">
    <Map/>
  </div>
{/if}
 
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  
  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }


  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    
  }

  
</style>
