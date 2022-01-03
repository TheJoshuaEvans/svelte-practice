<script>
  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();

  function sayHello() {
    /*
      The `type` here (first argument) can be any string as long as there is
      a listener listening to the corresponding `type` (on:<event-type>)
    */
    dispatch('message', {
      text: 'Hello!',
    });
  }
</script>

<button on:click={sayHello}>
	Click to say hello
</button>
