<script>
  import CustomButton from './CustomButton.svelte';
  import Inner from './Inner.svelte';
  import Outer from './Outer.svelte';

  function handleMessage(event) {
    alert(event.detail.text);
  }

  function handleClick() {
    alert('Button Clicked');
  }
</script>

<Inner on:message={handleMessage}/>
<Outer on:message={handleMessage}/>
<CustomButton on:click={handleClick}/>
