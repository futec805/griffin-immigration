<script lang="ts">
	import { page } from '$app/stores';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import WhatsAppButton from '$lib/components/WhatsAppButton.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<Header pathname={$page.url.pathname} />

<main class="min-h-screen">
	{@render children()}
</main>

<Footer />
<WhatsAppButton />
