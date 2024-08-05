<script>
	import Icon from '@iconify/svelte';
</script>

<div class="w-full bg-[#e5e7ef] py-24 px-5">
	<section class=" grid md:grid-cols-2 items-center gap-14 max-w-5xl mx-auto w-full px-2">
		<div class="flex flex-col text-left gap-5 md:gap-7">
			<p class="font-medium text-lg text-[#0FC1A7]">Feel Free To Contact Us</p>
			<h2 class="md:text-4xl text-3xl leading-none font-semibold text-black">Let’s Get in Touch</h2>
			<p class="text-lg">
				Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.
			</p>

			<div class="space-y-4">
				<div class="flex gap-3 text-lg font-medium items-center">
					<div class="size-7 rounded-full flex items-center justify-center bg-[#0FC1A7]">
						<Icon icon="material-symbols:mail" class="text-white text-lg" />
						<!-- <Icon icon="material-symbols/mail" /> -->
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
			<form
				action="https://formsubmit.co/info@e-prescribo.com"
				method="POST"
				class="flex flex-col gap-5"
			>
				<input type="hidden" name="_next" value="https://yourdomain.co/thanks.html" />
				<input type="hidden" name="_subject" value="New submission via Contact us!" />
				<input type="hidden" name="_captcha" value="false" />

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

				<div class="w-full px-4 py-2.5 border border-gray-300 rounded-lg">
					<select name="service" id="service" class="w-full outline-none ring-0">
						<option value="service1">Service 1</option>
						<option value="service2">Service 2</option>
						<option value="service3">Service 3</option>
						<option value="service4">Service 4</option>
					</select>
				</div>

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
