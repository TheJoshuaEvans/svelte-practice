<script>
  import Nested from './Nested.svelte';

  let name = 'world';
  let src = '/extremely-important-image.gif';
  let imgAltText = 'A dancing man. You could say he\'s really ROLLING with it';
</script>

<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 1.2em;
	}
</style>

<p>Hello {name.toUpperCase()}!</p>

<p>This is a paragraph. Please observe the following extremely important image </p>
<Nested/>
<img {src} alt="{imgAltText}" title="{imgAltText}">
