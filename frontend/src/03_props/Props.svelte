<script>
  import Info from './Info.svelte';
  import Nested from './Nested.svelte';

  const pkg = {
    name: 'svelte',
    version: 3,
    speed: 'blazing',
    website: 'https://svelte.dev',
  };
</script>

<Info {...pkg}/>

<Nested answer={42}/>
<Nested/>
