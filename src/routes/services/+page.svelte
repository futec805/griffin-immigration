<script lang="ts">
	import { services, site } from '$lib/site';

	const steps = [
		{ num: '01', title: 'Free Consultation', desc: 'Share your goals with us — we listen and understand your needs.' },
		{ num: '02', title: 'Personalized Plan', desc: 'Get a tailored roadmap based on your profile and preferred country.' },
		{ num: '03', title: 'Application & Prep', desc: 'We handle documentation, coaching, and the full application process.' },
		{ num: '04', title: 'Visa & Departure', desc: 'From visa filing to pre-departure guidance — we are with you till the end.' }
	];

	const reasons = [
		{ icon: '✅', title: '95% Visa Success Rate', desc: 'Proven results — over 500 successful visa approvals across all destinations.' },
		{ icon: '🎯', title: 'Personalized Guidance', desc: 'No cookie-cutter advice. Every plan is built around your unique goals.' },
		{ icon: '📋', title: 'End-to-End Support', desc: 'From course selection to pre-departure briefing — one team, every step.' },
		{ icon: '🏛️', title: 'Certified Consultants', desc: 'Experienced team with in-depth knowledge of global immigration systems.' },
		{ icon: '📚', title: 'In-House Coaching', desc: 'IELTS and PTE preparation at our own coaching centre — no third parties.' },
		{ icon: '💰', title: 'Transparent Pricing', desc: 'No hidden fees. Clear cost breakdown before you commit to anything.' }
	];
</script>

<svelte:head><title>Our Services — Griffin Immigration</title></svelte:head>

<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">Our Services</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">Everything you need for your study abroad and immigration journey — all under one roof.</p>
	</div>
</section>

<section class="py-12 md:py-20 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 lg:gap-8">
			{#each services as svc}
				<div class="group bg-white border border-slate-200 rounded-2xl p-6 md:p-8 hover:border-brand-400 hover:shadow-lg hover:shadow-brand-100/50 transition-all duration-300">
					<div class="w-14 h-14 bg-brand-50 rounded-xl flex items-center justify-center text-2xl mb-5 group-hover:bg-brand-100 transition-colors">
						{svc.icon}
					</div>
					<h3 class="text-xl font-bold text-slate-900 mb-3">{svc.title}</h3>
					<p class="text-slate-600 leading-relaxed text-sm">{svc.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-12 md:py-20 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-12">How We Work</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 lg:gap-8">
			{#each steps as step}
				<div class="text-center">
					<div class="w-12 h-12 bg-brand-500 text-white rounded-full flex items-center justify-center text-lg font-bold mx-auto mb-4">{step.num}</div>
					<h3 class="text-lg font-semibold text-slate-900 mb-2">{step.title}</h3>
					<p class="text-sm text-slate-500">{step.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-12 md:py-20 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-12">Why Students Choose Us</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each reasons as r}
				<div class="flex gap-4 p-5 rounded-xl bg-slate-50 border border-slate-100">
					<span class="text-2xl shrink-0 mt-0.5">{r.icon}</span>
					<div>
						<h3 class="font-semibold text-slate-900 mb-1">{r.title}</h3>
						<p class="text-sm text-slate-500 leading-relaxed">{r.desc}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-12 md:py-16 bg-gradient-to-br from-slate-900 to-brand-900 text-white">
	<div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-2xl md:text-4xl font-bold text-white mb-4">Not Sure Which Service You Need?</h2>
		<p class="text-slate-300 text-lg mb-8 max-w-2xl mx-auto">Talk to our experts for a free consultation. We'll assess your profile and recommend the best path forward.</p>
		<div class="flex flex-col sm:flex-row gap-4 justify-center">
			<a href="tel:{site.phone}" class="inline-flex items-center gap-2 px-8 py-4 text-lg font-semibold text-white bg-brand-600 hover:bg-brand-700 rounded-xl transition-colors shadow-lg shadow-brand-600/25">
				📞 Call {site.phone}
			</a>
			<a href="/contact" class="inline-flex items-center gap-2 px-8 py-4 text-lg font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-xl transition-colors shadow-lg shadow-accent-500/25">
				✉️ Send Enquiry
			</a>
		</div>
	</div>
</section>
