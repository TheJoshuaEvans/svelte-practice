<script>
  import InputField from './InputField.svelte';
  let field;
</script>

<button on:click="{() => field.focus()}">
  Focus field
</button>

<InputField bind:this={field} />
