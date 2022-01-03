<script>
	import Inner from './Inner.svelte';
</script>

<!--
  An `on:<event-type>` event directive without a value means 'forward all <event-type> events'
-->
<Inner on:message/>
