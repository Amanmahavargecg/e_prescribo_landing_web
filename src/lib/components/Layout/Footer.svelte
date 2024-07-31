<script>
	import Logo from '$lib/images/logo-white.svg';
	import Icon from '@iconify/svelte';

	const links = [
		{ text: 'Home', href: '/' },
		{ text: 'About', href: '/about-us' },
		{ text: 'Contact', href: '/contact-us' }
	];
</script>

<div class="w-full bg-[#0FC1A7] md:py-24 py-20 px-5">
	<section class="flex flex-col items-center justify-center gap-7 max-w-6xl mx-auto w-full px-2">
		<a href="/" class="flex items-center">
			<img src={Logo} alt="Logo" class="h-10 md:h-14" />
		</a>
		<div class="flex flex-wrap items-center justify-center gap-4">
			<a href="/contact-us" class="border-2 flex p-3 gap-2 rounded-xl text-white font-semibold">
				<Icon icon="lucide:send" class="text-white text-2xl" />
				Take a Appointment
			</a>
			<a
				href="https://api.whatsapp.com/send?phone=916352100733"
				class="border-2 flex p-3 gap-2 rounded-xl text-white font-semibold"
			>
				<Icon icon="mdi:whatsapp" class="text-white text-2xl" />
				Connect on Whatsapp
			</a>
		</div>
		<div class="flex">
			<ul
				class="flex gap-3 md:gap-5 flex-wrap items-center max-md:justify-center justify-evenly md:text-2xl"
			>
				{#each links as { text, href }}
					<li>
						<a class="text-white font-medium transition-colors" {href}>
							{text}
						</a>
					</li>
				{/each}
			</ul>
		</div>
	</section>
</div>
