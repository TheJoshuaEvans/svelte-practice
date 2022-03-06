<script>
  import TextInputs from './TextInputs.svelte';
  import NumericInputs from './NumericInputs.svelte';
  import CheckboxInputs from './CheckboxInputs.svelte';
  import GroupInputs from './GroupInputs.svelte';
  import TextareaInputs from './TextareaInputs.svelte';
  import SelectBindings from './SelectBindings.svelte';
  import ContentEditable from './ContentEditable.svelte';
  import EachBlockBindings from './EachBlockBindings.svelte';
  import MediaElements from './MediaElements.svelte';
  import Dimensions from './Dimensions.svelte';
  import This from './This.svelte';
  import ComponentBindings from './ComponentBindings.svelte';
  import ComponentInstances from './ComponentInstances.svelte';

  const inputDisplays = [
    {name: 'Text Inputs', component: TextInputs},
    {name: 'Numeric Inputs', component: NumericInputs},
    {name: 'Checkbox Inputs', component: CheckboxInputs},
    {name: 'Group Inputs and Select Multiple', component: GroupInputs},
    {name: 'Textarea Inputs', component: TextareaInputs},
    {name: 'Select Bindings', component: SelectBindings},
    {name: 'Content Editable', component: ContentEditable},
    {name: '"Each" Block Bindings', component: EachBlockBindings},
    {name: 'Media Elements', component: MediaElements},
    {name: 'Dimensions', component: Dimensions},
    {name: 'This', component: This},
    {name: 'ComponentBindings', component: ComponentBindings},
    {name: 'ComponentInstances', component: ComponentInstances},
  ].reverse();
</script>

{#each inputDisplays as {name, component}, i}
  <h3>{name}</h3>
  <svelte:component this={component}/>
  {#if i !== inputDisplays.length - 1}
    <hr>
  {/if}
{/each}
