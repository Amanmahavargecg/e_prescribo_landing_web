<script lang="ts">
	let data = [
		{
			title: 'Discover the Power of E-Prescribo',
			description:
				'With E-Prescribo, you can experience a new level of convenience and control over your health journey. Our platform is designed to be user-friendly, ensuring that you can easily manage your prescriptions and medical records without hassle.',
			button: 'Scheldue Appointment',
			image:
				'https://images.unsplash.com/photo-1471864190281-a93a3070b6de?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
		},
		{
			title: 'Be the part of organized healthcare',
			description:
				'Join us in transforming the future of healthcare. Experience the benefits of E-Prescribo today and take the first step towards a healthier, more organized life.',
			button: 'Scheldue Appointment',
			image:
				'https://images.unsplash.com/photo-1471864190281-a93a3070b6de?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
		}
	];
</script>

<section class="max-w-6xl mx-auto px-5 py-10">
	<div class="space-y-4">
		<h1 class="font-medium text-base tracking-wide uppercase">ABOUT US</h1>
		<h3 class="md:text-5xl text-3xl font-semibold">Welcome to E-Prescribo</h3>
		<p class="text-lg">Your Journey to Better Health Starts Here.</p>
	</div>

	<div class="md:mt-10 mt-5">
		<img
			src="https://images.unsplash.com/photo-1471864190281-a93a3070b6de?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
			alt=""
			class="w-full md:h-[400px] object-cover rounded-2xl object-center"
		/>
	</div>
	<div class="space-y-6 text-center mt-10">
		<h1 class="text-base font-medium uppercase">Our Story</h1>
		<h3 class="lg:text-4xl md:ext-3xl text-2xl font-semibold capitalize">
			Everyone has their own story to tell
		</h3>
		<div class="md:w-11/12 mx-auto space-y-3 text-lg">
			<p>
				At E-Prescribo, we are committed to revolutionizing the way you manage your health. Our journey began with a simple yet powerful idea: to make healthcare more accessible, efficient, and personalized through innovative technology.
			</p>
			<p>
				In a world where healthcare systems can often be complex and fragmented, E-Prescribo was created to bridge gaps and simplify the process. We understand that managing prescriptions and medical records can be overwhelming, which is why we've designed our platform to provide a seamless experience for both patients and healthcare providers.
			</p>
		</div>
	</div>
</section>
<section>
	{#each data as d, i}
		<section class=" grid md:grid-cols-2 my-24 items-start gap-14 max-w-6xl mx-auto w-full px-5">
			<div class="space-y-7">
				<h2 class=" text-3xl md:text-4xl font-serif font-semibold text-black">
					{d.title}
				</h2>
				<p class="text-lg">
					{d.description}
				</p>
				<button
					class="w-fit text-nowrap h-max text-lg font-semibold px-8 py-2 rounded-full text-white bg-[#0FC1A7]"
				>
					{d.button}
				</button>
			</div>
			<div
				class={`h-auto rounded-xl bg-[#0FC1A7] w-full ${i % 2 == 0 ? 'order-last' : 'order-first'}`}
			>
				<div
					class="h-auto rounded-xl bg-white -rotate-3 w-full flex flex-wrap items-center justify-between"
				>
					<img
						class="h-full w-full object-cover rounded-2xl bg-gray-300 max-md:order-first"
						src={d.image}
						alt=""
					/>
				</div>
			</div>
		</section>
	{/each}
</section>
