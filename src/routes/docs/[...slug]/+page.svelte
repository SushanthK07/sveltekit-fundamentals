<script>
	import { page } from '$app/stores';

	const slugArray = $page.params.slug.split('/');
	console.log(slugArray);
</script>

{#if slugArray.length === 1}
	<h3>Docs for Feature {slugArray[0]}</h3>
{:else if slugArray.length === 2}
	<h3>Docs for Feature {slugArray[0]} > Concept {slugArray[1]}</h3>
{:else if slugArray.length === 3}
	<h3>
		Docs for Feature {slugArray[0]} > Concept {slugArray[1]} > Example {slugArray[2]}
	</h3>
{:else}
	<h3>Docs for {$page.params.slug} page</h3>
{/if}
