<script>
  import C_Table from './Table.svelte';
  export let title;
  export let table_data;
</script>

<div class="collapsible-header">{title}</div>
<div class="collapsible-body">
    <C_Table data={table_data}/>
</div>