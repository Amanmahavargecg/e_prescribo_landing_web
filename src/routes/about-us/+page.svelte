<script lang="ts">
	let data = [
		{
			title: 'Discover the Power of Our Products',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod. Quisquam, quod. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod. Quisquam, quod.',
			button: 'Scheldue Appointment',
			image:
				'https://images.unsplash.com/photo-1471864190281-a93a3070b6de?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
		},
		{
			title: 'Discover the Power of Our Products',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod. Quisquam, quod. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod. Quisquam, quod.',
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
				Lorem ipsum dolor, sit amet consectetur adipisicing elit. Inventore ipsum, quam, quia animi
				minus laudantium voluptates consectetur facilis veritatis at officiis perferendis cum
				debitis dolor quis quae adipisci laboriosam quo. Lorem ipsum dolor, sit amet consectetur
				adipisicing elit. Ratione quasi totam corporis sapiente numquam esse fugit iusto deleniti,
				quam repellat, similique inventore vel! Libero rerum accusamus vel et ea aperiam omnis
				consequatur laborum dolore eligendi? Eius inventore qui similique soluta quo quas ipsa
				consequuntur beatae.
			</p>
			<p>
				Praesentium obcaecati, a ex sequi blanditiis ducimus. Consectetur nemo sunt molestiae quos,
				esse voluptatibus expedita, voluptatum distinctio dicta odit quidem animi. Pariatur, tenetur
				modi cum, odio soluta accusamus mollitia non ullam nobis ab, facere assumenda! Minima dicta
				aspernatur, quod aperiam dolor repellat delectus maxime, atque voluptatem officia fugit
				incidunt facere dignissimos magnam! Temporibus, magni dicta.
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
