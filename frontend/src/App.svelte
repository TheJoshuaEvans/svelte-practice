<script>
  import Introduction from './01_introduction/Introduction.svelte';
  import Reactivity from './02_reactivity/Reactivity.svelte';
  import Props from './03_props/Props.svelte';
  import Logic from './04_logic/Logic.svelte';

  // Load chapters in reverse order so the latest one is at the top of the page
  const chapters = [
    Introduction, Reactivity, Props, Logic,
  ].reverse();
</script>

<style>
  div.chapter-container {
    border: 1px solid black;
    padding: 0.5em;
    margin-bottom: 1em;
  }

  h2 {
    margin-top: 0px;
  }
</style>

<h1>Svelte Practice</h1>
{#each chapters as chapter}
  <div class="chapter-container">
    <h2>{chapter.name}</h2>
    <svelte:component this={chapter}/>
  </div>
{/each}
