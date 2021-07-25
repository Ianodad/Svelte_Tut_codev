<script>
	const names= [
		{
			firstName:'Bruce',
			lastName:'Wayne'
		},
		{
			firstName:'Clark',
			lastName:'Knet'
		},
		{
			firstName:'You',
			lastName:'Tube'
		}
	]
</script>

{#each names as name (name)}
	<slot name="hero" firstName={name.firstName} lastName={name.lastName}/>	
{/each}