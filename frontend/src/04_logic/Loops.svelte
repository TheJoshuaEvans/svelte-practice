<script>
  let cats = [
    { id: 'J---aiyznGQ', name: 'Keyboard Cat' },
    { id: 'z_AbfPXTKms', name: 'Maru' },
    { id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' },
  ];

  import Thing from './Thing.svelte';

  let things = [
    { id: 1, name: 'apple' },
    { id: 2, name: 'banana' },
    { id: 3, name: 'carrot' },
    { id: 4, name: 'doughnut'},
    { id: 5, name: 'egg' },
  ];
  let thingsCount = 5;

  function handleRemoveThing() {
    things = things.slice(1);
  }

  function handleAddThing() {
    things = [ ...things, {
      id: thingsCount + 1,
      name: 'thing ' + (thingsCount + 1),
    }];
    thingsCount++;
  }
</script>

<button on:click={handleRemoveThing}>
	Remove first thing
</button>

<button on:click={handleAddThing}>
	Add thing
</button>

<!--
  My Hypothesis:
  The interaction between loops and the DOM is interesting. Components are not deleted and
  recreated every single time a loop like this is run. Instead, the existing components are
  modified in-place and - by default - any new items in the array being looped through will be
  added as new components to the _end_ of the component list. If any items were deleted, the
  final DOM component will be removed to make the number of elements match

  This can be worked around with the "key" syntax below `... (thing.id)}`. This syntax will tell
  Svelte what key to use when matching items in the array with DOM components, so that the
  correct components can be removed, and new components will go into the correct spot

  Seems to me that, as a rule of thumb, it would be a good idea to identify the object key
  whenever possible to avoid unexpected behavior
-->
{#each things as thing, i (thing.id)}
	<Thing name={thing.name} index={i}/>
{/each}

<h4>The Famous Cats of YouTube</h4>

<ul>
  <!-- Key identification syntax also works with destructuring -->
  {#each cats as {id, name}, i (id)}
    <li><a target="_blank" href="https://www.youtube.com/watch?v={id}">
      {i+1}: {name}
    </a></li>
  {/each}
</ul>
