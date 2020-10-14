<script>
  import C_Row from './Row.svelte';
  export let data;
</script>

<main>
  
  <table class="centered" >
    
    <thead>
      <tr>
        <th>Tool</th>
        <th>State</th>
        <th>Info</th>
      </tr>
    </thead>

    <tbody>
      {#each data as d}
        <C_Row {...d}/>
      {/each}
    </tbody>

  
  </table>
</main>
