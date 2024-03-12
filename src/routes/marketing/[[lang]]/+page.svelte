<script>
	import { page } from '$app/stores';

	const greet = {
		en: 'Hello',
		es: 'Hola',
		fr: 'Bonjour',
		hi: 'Namaste',
		te: 'హలో'
	};

	const lang = $page.params.lang || 'en';
	const message = greet[lang];
</script>

<h1>{message}</h1>
