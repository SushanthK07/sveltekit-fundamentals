<script>
	import { goto, beforeNavigate, afterNavigate } from '$app/navigation';

	const handleOrder = () => {
		goto('/products');
		// goto('/products', { replaceState: true });
	};

	beforeNavigate((navigation) => {
		console.log('Before navigate', navigation);
	});

	afterNavigate((navigation) => {
		console.log('After navigate', navigation);
	});
</script>

<h1>Home page</h1>

<a href="/about">About</a>
<a href="/blog">Blog</a>
<a href="/docs">Docs</a>
<a href="/marketing">Marketing</a>
<a href="/profile">Profile</a>
<a href="/products">Products</a>

<button on:click={handleOrder}>Place Order</button>
