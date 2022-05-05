<template>
 <!-- Hire me -->
		<div class="container mt-64 flex justify-between items-center mx-auto px-8 md:px-14 lg:px-24 w-full">
			<section class="w-full">
				<h2 id="hire" class="secondary-title">Hire me</h2>
				<p class="section-paragraph">Feel free to to contact me any time, through any method below.</p>

				<div class="w-full grid lg:grid-cols-2 gap-8 lg:gap-32 mt-24">
					<div class="space-y-12">
						<div>
							<label class="text-white block mb-6 text-xl font-bold">Name</label>
							<input class="w-full border border-input-border bg-input px-4 py-4">
						</div>
						<div>
							<label class="text-white block mb-6 text-xl font-bold">Email</label>
							<input type="email" class="w-full border border-input-border bg-input px-4 py-4">
						</div>
						<div>
							<label class="text-white block mb-6 text-xl font-bold">Message</label>
							<textarea type="email" class="w-full border border-input-border bg-input px-4 py-4 h-56 resize-none"></textarea>
						</div>
						<button class="px-6 py-2 bg-theme text-white font-bold">Send it!</button>
					</div>

					<div class="mt-12">
						<!-- Contact info -->
						<p class="text-secondary">0857-3201-2292</p>
						<a href="mailto:avrilalelia01@gmail.com" class="text-secondary underline mt-3 block">avrilalelia01@gmail.com</a>

						<!-- Socials -->
						<div class="flex mt-20 space-x-6">
							<!-- Linkedin -->
							<a href="https://www.linkedin.com/in/avril-alelia/">
								<img src="../assets/in.png" width="42" height="42" alt="LinkedIn Logo">
							</a>
							<!-- Github -->
							<a href="https://github.com/avrilalelia">
								<img src="../assets/github.png" width="42" height="42" alt="LinkedIn Logo">
							</a>
						</div>
					</div>
					
				</div>

			</section>
		</div>
</template>

<script>
export default {
 name: 'HireMePart',
 setup(){
 }
}
</script>
