<script>
  let count = 0;
  $: doubled = count * 2;

  $: {
    console.log('The current count is ' + count);
    console.log('...which when doubled becomes ' + doubled);

    if (count >= 5) {
      console.warn('Count approaching dangerous levels!');
    }
  }

  $: if (count >= 10) {
    alert('Count is dangerously high!');
    count = 9;
  }

  function incrementCount() {
    count += 1;
  }
</script>

<h3>Counting</h3>
<button on:click={incrementCount}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
<p>{count} doubled is {doubled}</p>
