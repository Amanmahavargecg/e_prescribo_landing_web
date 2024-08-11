<script lang="ts">
	import { onMount } from 'svelte';
	import { writable, derived } from 'svelte/store';
	import { page } from '$app/stores';
	import Logo from '$lib/images/logo.svg';
	import Icon from '@iconify/svelte';

	const isSticky = false;
	const links = [
		{ text: 'Home', href: '/' },
		{ text: 'About', href: '/about-us' },
		{ text: 'Contact', href: '/contact-us' }
	];

	let isMobileMenuOpen = writable(false);
	let scrollbind = writable(0);

	const isScrolled = derived(scrollbind, $scrollbind => $scrollbind > 40);

	function isActive(href: string) {
		return href === $page.url.pathname;
	}

	function toggleMobileMenu() {
		isMobileMenuOpen.update(isOpen => !isOpen);
	}

	onMount(() => {
		const handleScroll = () => {
			scrollbind.set(window.scrollY);
		};
		window.addEventListener('scroll', handleScroll);
		return () => {
			window.removeEventListener('scroll', handleScroll);
		};
	});
</script>

<header
	class="top-0 md:mt-5 z-40 relative mx-auto w-full border-b border-gray-50/0 transition-all duration-300 ease-in-out {isScrolled ? 'bg-white shadow-md sticky' : ''}"
	data-aw-sticky-header={isSticky}
>
	<div class="relative py-5 px-3 md:px-6 mx-auto max-w-6xl flex justify-between bg-white items-center">
		<div class="flex max-md:w-full justify-between items-center">
			<a href="/" class="flex items-center">
				<img src={Logo} alt="Logo" class="h-8" />
			</a>
			<button class="md:hidden text-gray-500 hover:text-gray-700" on:click={toggleMobileMenu}>
				<Icon icon={$isMobileMenuOpen ? 'tabler:x' : 'tabler:menu-2'} class="w-6 h-6" />
			</button>
		</div>

		<nav class="hidden md:flex items-center w-auto mx-5" aria-label="Main navigation">
			<ul class="flex text-[0.9375rem] tracking-[0.01rem] font-medium">
				{#each links as { text, href }}
					<li>
						<a
							class="px-4 py-3 flex items-center hover:text-[#0FC1A7] transition-colors {isActive(href) ? 'text-[#0FC1A7]' : ''}"
							href={href}
						>
							{text}
						</a>
					</li>
				{/each}
			</ul>
		</nav>

		<div class="hidden md:flex gap-7 items-center">
			<div class="flex items-center gap-2">
				<Icon icon="ic:sharp-whatsapp" class="text-[#0FC1A7] text-2xl" />
				<a
					class="py-3 underline underline-offset-4 text-[#0FC1A7] hover:text-[#0DA090] transition-colors"
					href="https://api.whatsapp.com/send?phone=916352100733"
				>
					Connect on Whatsapp
				</a>
			</div>
			<a
				href="/contact-us"
				class="text-lg font-semibold px-4 py-3 rounded-lg text-white bg-[#0FC1A7] hover:bg-[#0DA090] transition-colors"
			>
				Appointment
			</a>
		</div>
	</div>

	<!-- Mobile Menu -->
	{#if $isMobileMenuOpen}
		<div class="md:hidden bg-white absolute top-full left-0 right-0 shadow-md">
			<nav class="px-4 py-2" aria-label="Mobile navigation">
				<ul class="flex flex-col space-y-2">
					{#each links as { text, href }}
						<li>
							<a
								class="block py-2 px-4 hover:bg-gray-100 {isActive(href) ? 'text-[#0FC1A7]' : ''}"
								href={href}
								on:click={toggleMobileMenu}
							>
								{text}
							</a>
						</li>
					{/each}
				</ul>
			</nav>
			<div class="px-4 py-4 space-y-4">
				<div class="flex items-center gap-2">
					<Icon icon="ic:sharp-whatsapp" class="text-[#0FC1A7] text-2xl" />
					<a
						class="py-2 underline underline-offset-4 text-[#0FC1A7]"
						href="https://api.whatsapp.com/send?phone=916352100733"
					>
						Connect on Whatsapp
					</a>
				</div>
				<a
					href="/contact-us"
					class="w-full text-lg font-semibold px-4 py-3 rounded-lg text-white bg-[#0FC1A7] hover:bg-[#0DA090] transition-colors"
				>
					Appointment
				</a>
			</div>
		</div>
	{/if}
</header>
