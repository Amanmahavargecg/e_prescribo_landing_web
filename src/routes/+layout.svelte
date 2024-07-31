<script>
	import Footer from '$lib/components/Layout/Footer.svelte';
	import Header from '$lib/components/Layout/Header.svelte';

	// import Header from './Header.svelte';
	import '../app.css';
</script>

<div class="app 2xl:text-[20px] bg-[#F8F9FE]">
	<div class="w-full py-2 h-10 bg-[#0FC1A7]"></div>
	<Header />
	<main class="antialiased text-default bg-page tracking-tight">
		<slot />
	</main>
	<Footer />
</div>
