<script>
	import {getContext} from 'svelte';

const chan = getContext('chan-context')
</script>

<h2>Child F Component</h2>

<p>This is {chan}</p>
