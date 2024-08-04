<script>
	import HeroIcon from '$lib/images/heroicon.png';
	import Pattern1 from '$lib/images/pattern1.svg';
	import Logo from '$lib/images/logo-white.svg';
	import Icon from '@iconify/svelte';
	const contentArray1 = [
		{
			title: 'Electronic Prescription',
			description: 'Send Prescriptions to your pharmacies with just a few clicks of a button',
			image:
				'https://images.unsplash.com/photo-1471864190281-a93a3070b6de?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
		},
		{
			title: 'Paitent Profile Management',
			description: 'Easily manage your patient profiles and their medical history with ease',
			image:
				'https://plus.unsplash.com/premium_photo-1682141162813-16fc10b5ba2f?q=80&w=3132&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
		},
		{
			title: 'Medicine Histrory Tracking',
			description: 'Track the medicine history of your patients and their prescriptions with ease',
			image:
				'https://images.unsplash.com/photo-1516826435551-36a8a09e4526?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
		}
	];
	let selectedContent1 = $state(0);

	const flowArray = [
		{
			title: 'Sign Up',
			description: 'Send Prescriptions to your pharmacies with just a few clicks of a button'
		},
		{
			title: 'Schedule Appointment',
			description: 'Easily manage your patient profiles and their medical history with ease'
		},
		{
			title: 'Receive Prescription',
			description: 'Track the medicine history of your patients and their prescriptions with ease'
		},
		{
			title: 'Order Medicine',
			description: 'Track the medicine history of your patients and their prescriptions with ease'
		}
	];

	const whyChooseUs = [
		'Safety First Quality Must',
		'Always on Time',
		'Patient Satisfaction',
		'Cuttting Edge Technology',
		'Transperant Pricing'
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="px-2">
	<div
		class="h-[70svh] max-w-6xl mx-auto justify-center py-10 flex-wrap items-center flex gap-5 md:gap-10"
	>
		<img src={HeroIcon} alt="Hero Icon" class="h-36 md:h-52" />
		<div class="max-w-md flex flex-col max-md:text-center max-md:items-center">
			<h1 class="text-xl font-medium text-[#0FC1A7]">Welcome to E-Prescribo</h1>
			<p class=" text-5xl md:text-6xl leading-none md:leading-tight font-semibold text-black mt-5">
				Your Journey to Better Health Starts Here
			</p>
			<button class="w-max mt-7 text-lg font-semibold px-4 py-3 rounded-lg text-white bg-[#0FC1A7]">
				Connect with us
			</button>
		</div>
	</div>
</section>

<section class=" grid md:grid-cols-2 items-center gap-10 md:gap-12 max-w-6xl mx-auto w-full px-5">
	<div class="flex flex-col gap-8 md:gap-12">
		{#each contentArray1 as { title, description, image }, i}
			<button
				onclick={() => (selectedContent1 = i)}
				class="flex flex-col text-left gap-4 {i === selectedContent1
					? 'border-l-2 pl-5 border-black'
					: 'border-l-2 pl-5 border-transparent'}"
			>
				<h2 class="md:text-4xl font-serif font-semibold text-black">{title}</h2>
				<p class="text-lg">{description}</p>
			</button>
		{/each}
	</div>

	<img
		class="h-full w-full object-cover rounded-2xl bg-gray-300 max-md:order-first"
		src={contentArray1[selectedContent1].image}
		alt=""
	/>
</section>

<section class="max-w-6xl mx-auto px-5 mt-24">
	<div class="h-auto rounded-xl bg-[#0FC1A7] w-full">
		<div
			class="h-auto rounded-xl bg-white -rotate-2 w-full flex flex-wrap items-center justify-between py-10 px-8 md:py-14 md:px-10"
		>
			<div class="flex flex-col gap-5 py-10">
				<h2 class=" text-3xl md:text-4xl font-serif font-semibold text-black">
					Streamline your prescription management ?
				</h2>
				<p class="text-lg">
					Get ready for fast, cool and hurdle free prescription management
				</p>
			</div>
			<a
				href="/contact-us"
				class="w-fit text-nowrap h-max text-lg font-semibold px-8 py-3 rounded-full text-white bg-[#0FC1A7]"
			>
				Scheldue Appointment
			</a>
		</div>
	</div>
</section>

<section
	class=" mt-24 grid md:grid-cols-2 items-center gap-10 md:gap-12 max-w-6xl mx-auto w-full px-5"
>
	<img
		class="h-full w-full object-cover rounded-2xl bg-gray-300 max-md:order-first"
		src={contentArray1[selectedContent1].image}
		alt=""
	/>
	<div class="flex flex-col gap-8 md:gap-12">
		{#each contentArray1 as { title, description, image }, i}
			<button
				onclick={() => (selectedContent1 = i)}
				class="flex flex-col text-left gap-4 {i === selectedContent1
					? 'border-l-2 pl-5 border-black'
					: 'border-l-2 pl-5 border-transparent'}"
			>
				<h2 class="md:text-4xl font-serif font-semibold text-black">{title}</h2>
				<p class="text-lg">{description}</p>
			</button>
		{/each}
	</div>
</section>

<section class=" grid md:grid-cols-2 mt-24 items-start gap-14 max-w-6xl mx-auto w-full px-5">
	<div class="flex flex-col text-left gap-7">
		<h2 class=" text-3xl md:text-4xl font-serif font-semibold text-black">
			Discover the Power of E-Prescribo
		</h2>
		<p class="text-lg">
			With E-Prescribo, you can experience a new level of convenience and control over your health journey. Our platform is designed to be user-friendly, ensuring that you can easily manage your prescriptions and medical records without hassle
		</p>
		<button
			class="w-fit text-nowrap h-max text-lg font-semibold px-8 py-2 rounded-full text-white bg-[#0FC1A7]"
		>
			Scheldue Appointment
		</button>
	</div>

	<div class="flex flex-col gap-4 md:gap-8">
		{#each flowArray as { title, description }, i}
			<div
				class="flex flex-col p-7 gap-4 text-left {i % 2 == 0
					? ' bg-white rounded-xl md:-rotate-3  -rotate-1'
					: 'bg-[#0FC1A7] rounded-xl md:rotate-3 rotate-1'}"
			>
				<div class="flex justify-between">
					<h2 class="md:text-3xl font-serif font-semibold text-black">{title}</h2>
					<h2 class="md:text-3xl font-serif font-semibold text-black">0{i + 1}</h2>
				</div>
				<p class="text-lg w-full text-center">{description}</p>
			</div>
		{/each}
	</div>
</section>

<section class="mt-20 flex items-center justify-center gap-10 max-w-6xl w-full mx-auto">
	<img src={Pattern1} class=" hidden md:flex flex-1 md:max-w-[30%]" alt="" />
	<div class="flex items-center text-center justify-center gap-3 flex-col">
		<h2 class="md:text-4xl text-3xl font-semibold text-black">Why Choose Us?</h2>
		<ul class="space-y-2 mt-5">
			{#each whyChooseUs as item}
				<li class="text-lg flex gap-2 items-center">
					<Icon icon="icon-park-solid:check-one" class="text-[#0FC1A7] text-xl" />
					{item}
				</li>
			{/each}
		</ul>
	</div>
	<img src={Pattern1} class=" hidden md:flex flex-1 md:max-w-[30%]" alt="" />
</section>

<section class="mt-20 max-w-6xl px-8 md:px-10 w-full mx-auto">
	<div class="md:w-4/5 mx-auto">
		<h1 class="text-4xl font-semibold">Wellness, Compassion, Quality</h1>
		<p class="text-lg mt-5">
			We envision a future where healthcare is as straightforward as possible, where technology enhances the quality of care, and where every individual has the tools they need to make informed health decisions.
		</p>

		<button
			class="w-fit mt-5 text-nowrap h-max text-lg font-semibold px-6 py-3 rounded-xl text-white bg-[#0FC1A7]"
		>
			Take an Appointment
		</button>
	</div>
</section>

<div class="w-full bg-[#e5e7ef] mt-24 py-24 px-5">
	<section class=" grid md:grid-cols-2 items-center gap-14 max-w-5xl mx-auto w-full px-2">
		<div class="flex flex-col text-left gap-5 md:gap-7">
			<p class="font-medium text-[#0FC1A7]">APPOINTMENT</p>
			<h2 class="md:text-4xl text-3xl leading-none font-semibold text-black">
				Get in touch to book your first appointment
			</h2>
			<p class="text-lg">
				Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.
			</p>

			<div class="space-y-4">
				<div class="flex gap-3 text-lg font-medium items-center">
					<div class="size-7 rounded-full flex items-center justify-center bg-[#0FC1A7]">
						<Icon icon="ic:sharp-whatsapp" class="text-white text-lg" />
					</div>
					<a href="mailto:info@e-prescribo.com" class="hover:text-[#0DA090] transition-colors">
						info@e-prescribo.com
					</a>
				</div>
				<div class="flex gap-3 text-lg font-medium items-center">
					<div class="size-7 rounded-full flex items-center justify-center bg-[#0FC1A7]">
						<Icon icon="ic:sharp-phone" class="text-white text-lg" />
					</div>
					<a href="tel:+91 6352100733" class="hover:text-[#0DA090] transition-colors">
						+91 6352100733
					</a>
				</div>
			</div>

			<!-- <button
				class="w-fit text-nowrap h-max text-lg font-semibold px-8 py-2 rounded-full text-white bg-[#0FC1A7]"
			>
				Scheldue Appointment
			</button> -->
		</div>

		<div class="bg-white rounded-2xl p-8">
			<form action="" class="flex flex-col gap-5">
				<input
					type="text"
					id="name"
					placeholder="Name"
					name="name"
					class="w-full px-4 py-2.5 border border-gray-300 rounded-lg"
				/>

				<input
					type="email"
					placeholder="Email"
					id="email"
					name="email"
					class="w-full px-4 py-2.5 border border-gray-300 rounded-lg"
				/>

				<input
					type="tel"
					placeholder="Phone"
					id="phone"
					name="phone"
					class="w-full px-4 py-2.5 border border-gray-300 rounded-lg"
				/>

<!--
				<div class="w-full px-4 py-2.5 border border-gray-300 rounded-lg">
					<select name="service" id="service" class="w-full outline-none ring-0">
						<option value="service1">Service 1</option>
						<option value="service2">Service 2</option>
						<option value="service3">Service 3</option>
						<option value="service4">Service 4</option>
					</select>
				</div>
				-->

				<textarea
					name="message"
					id="message"
					cols="30"
					rows="3"
					class="w-full px-4 py-2.5 border border-gray-300 rounded-lg"
				></textarea>

				<button class="w-full text-lg font-semibold px-4 py-2.5 rounded-lg text-white bg-[#0FC1A7]">
					Scheldue Appointment
				</button>
			</form>
		</div>
	</section>
</div>
