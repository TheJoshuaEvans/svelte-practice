<script>
  let numbers = [1, 2, 3, 4];

  function addNumber() {
    numbers = [...numbers, numbers.length + 1];

    // This doesn't work since it doesn't trigger a reload!
    // Reactivity in Svelte is triggered by assignments, not method usage
    // numbers.push(numbers.length + 1);
  }

  $: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<h3>Adding Numbers</h3>
<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>
