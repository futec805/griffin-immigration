<script lang="ts">
	import { site } from '$lib/site';
</script>

<svelte:head><title>Contact Us — Griffin Immigration</title></svelte:head>

<!-- ===== HERO ===== -->
<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">Contact Us</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">Visit our office or drop us a message. We'd love to hear from you.</p>
	</div>
</section>

<!-- ===== CONTACT INFO + MAP ===== -->
<section class="py-12 md:py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-8 lg:gap-12">

			<!-- Left: Contact Info Box -->
			<div class="space-y-6">
				<div class="p-6 rounded-xl bg-slate-50 border border-slate-200">
					<h3 class="font-semibold text-slate-900 mb-5">Contact Info</h3>
					<ul class="space-y-5 text-sm">
						<li class="flex items-start gap-3">
							<span class="text-xl shrink-0 mt-0.5">📍</span>
							<div>
								<div class="font-semibold text-slate-800">Our Office</div>
								<p class="text-slate-500 mt-0.5 leading-relaxed">{site.address}</p>
							</div>
						</li>
						<li class="flex items-center gap-3">
							<span class="text-xl shrink-0">📞</span>
							<div>
								<div class="font-semibold text-slate-800">Phone / WhatsApp</div>
								<a href="tel:{site.phone}" class="text-brand-600 hover:text-brand-700 font-medium">{site.phone}</a>
							</div>
						</li>
						<li class="flex items-center gap-3">
							<span class="text-xl shrink-0">✉️</span>
							<div>
								<div class="font-semibold text-slate-800">Email</div>
								<a href="mailto:{site.email}" class="text-brand-600 hover:text-brand-700 font-medium break-all">{site.email}</a>
							</div>
						</li>
						<li class="flex items-center gap-3">
							<span class="text-xl shrink-0">🕐</span>
							<div>
								<div class="font-semibold text-slate-800">Working Hours</div>
								<p class="text-slate-500 mt-0.5">{site.hours}</p>
							</div>
						</li>
					</ul>
				</div>
			</div>

			<!-- Right: Google Map -->
			<div class="rounded-xl overflow-hidden border border-slate-200 shadow-sm h-full min-h-[280px]">
				<iframe
					src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3491.5!2d77.0!3d28.98!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390db490d7ce4819%3A0x4b473d7ad181f814!2sMayur%20Vihar%2C%20Sonipat%2C%20Haryana!5e0!3m2!1sen!2sin!4v1710000000000"
					width="100%"
					height="100%"
					style="border:0;"
					allowfullscreen=""
					loading="lazy"
					referrerpolicy="no-referrer-when-downgrade"
					title="Griffin Immigration Office Location"
				></iframe>
			</div>

		</div>
	</div>
</section>

<!-- ===== SEND US A MESSAGE ===== -->
<section id="message-form" class="py-12 md:py-16 bg-slate-50">
	<div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-8">
			<h2 class="text-2xl md:text-3xl font-extrabold text-slate-900">Send Us a Message</h2>
			<p class="text-slate-500 mt-2">Fill out the form below and we'll get back to you within 24 hours.</p>
		</div>

		<form class="bg-white p-6 md:p-8 rounded-xl border border-slate-200 shadow-sm space-y-5">
			<div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
				<div>
					<label for="name" class="block text-sm font-medium text-slate-700 mb-1.5">Full Name *</label>
					<input id="name" type="text" required class="w-full px-4 py-3 rounded-lg border border-slate-300 text-sm focus:border-brand-500 focus:ring-2 focus:ring-brand-100 outline-none transition-colors" placeholder="Your name" />
				</div>
				<div>
					<label for="email" class="block text-sm font-medium text-slate-700 mb-1.5">Email *</label>
					<input id="email" type="email" required class="w-full px-4 py-3 rounded-lg border border-slate-300 text-sm focus:border-brand-500 focus:ring-2 focus:ring-brand-100 outline-none transition-colors" placeholder="your@email.com" />
				</div>
			</div>
			<div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
				<div>
					<label for="phone" class="block text-sm font-medium text-slate-700 mb-1.5">Phone *</label>
					<input id="phone" type="tel" required class="w-full px-4 py-3 rounded-lg border border-slate-300 text-sm focus:border-brand-500 focus:ring-2 focus:ring-brand-100 outline-none transition-colors" placeholder="+91 98765 43210" />
				</div>
				<div>
					<label for="service" class="block text-sm font-medium text-slate-700 mb-1.5">Service</label>
					<select id="service" class="w-full px-4 py-3 rounded-lg border border-slate-300 text-sm text-slate-700 focus:border-brand-500 focus:ring-2 focus:ring-brand-100 outline-none transition-colors">
						<option value="">Select a service</option>
						<option>Student Visa</option>
						<option>Work Visa & PR</option>
						<option>IELTS Coaching</option>
						<option>PTE Coaching</option>

						<option>Other</option>
					</select>
				</div>
			</div>
			<div>
				<label for="country" class="block text-sm font-medium text-slate-700 mb-1.5">Preferred Country</label>
				<select id="country" class="w-full px-4 py-3 rounded-lg border border-slate-300 text-sm text-slate-700 focus:border-brand-500 focus:ring-2 focus:ring-brand-100 outline-none transition-colors">
					<option value="">Select country</option>
					<option>Canada</option>
					<option>Australia</option>
					<option>UK</option>
					<option>Germany</option>
					<option>USA</option>
					<option>Czech Republic</option>
					<option>Not sure yet</option>
				</select>
			</div>
			<div>
				<label for="message" class="block text-sm font-medium text-slate-700 mb-1.5">Message *</label>
				<textarea id="message" required rows="4" class="w-full px-4 py-3 rounded-lg border border-slate-300 text-sm focus:border-brand-500 focus:ring-2 focus:ring-brand-100 outline-none transition-colors resize-none" placeholder="Tell us about your goals and how we can help..."></textarea>
			</div>
			<button type="submit" class="w-full sm:w-auto px-8 py-3.5 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">
				Send Message
			</button>
		</form>
	</div>
</section>
