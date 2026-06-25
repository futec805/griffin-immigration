<script lang="ts">
	import { site } from '$lib/site';

	const directors = [
		{ name: 'Naveen Malik', role: 'Founder & Director', bio: 'With extensive experience in immigration consulting, Naveen leads the strategic vision of Griffin Immigration. His commitment to ethical practice and client success has helped hundreds of students and professionals achieve their dreams abroad.' }
	];

	const values = [
		{ title: 'Integrity', desc: 'Honest, transparent advice — we never promise what we cannot deliver.' },
		{ title: 'Excellence', desc: 'Meticulous attention to detail in every application we handle.' },
		{ title: 'Client First', desc: 'Your goals drive our decisions. Personalized solutions, not one-size-fits-all.' },
		{ title: 'Results', desc: 'Proven track record with 95% visa success rate and 500+ approvals.' }
	];
</script>

<svelte:head><title>About Us — Griffin Immigration</title></svelte:head>

<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">About Us</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">We're on a mission to make global education and immigration accessible, transparent, and successful for every aspiring student and professional.</p>
	</div>
</section>

<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="max-w-3xl mx-auto text-center">
			<h2 class="text-2xl md:text-3xl font-bold text-slate-900 mb-6">Our Story</h2>
			<p class="text-slate-500 leading-relaxed mb-4">
				Griffin Immigration Private Limited was founded with a simple belief: every talented student and professional deserves access to global opportunities. Based in Sonipat, Haryana, we have grown from a small consultancy into a trusted partner for hundreds of students and skilled workers seeking to study, work, and settle abroad.
			</p>
			<p class="text-slate-500 leading-relaxed mb-4">
				Our team combines deep knowledge of international education systems with hands-on expertise in visa processing, documentation, and compliance. We serve as a one-stop destination — offering university selection, admission guidance, SOP writing, visa filing, and IELTS/PTE coaching — all under one roof.
			</p>
			<p class="text-slate-500 leading-relaxed">
				Incorporated in August 2022 (CIN: U74999HR2022PTC106123), we are committed to the highest standards of professional ethics and client service. Every application we handle goes through a rigorous quality check to maximize your chances of success.
			</p>
		</div>
	</div>
</section>

<section class="py-16 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-12">Our Values</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
			{#each values as v}
				<div class="p-6 rounded-xl bg-white border border-slate-200 text-center">
					<h3 class="text-lg font-bold text-brand-600 mb-2">{v.title}</h3>
					<p class="text-sm text-slate-500 leading-relaxed">{v.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-12">Leadership</h2>
		<div class="max-w-md mx-auto">
			{#each directors as d}
				<div class="p-6 rounded-xl border border-slate-200 bg-white text-center">
					<div class="w-20 h-20 mx-auto rounded-full bg-brand-100 flex items-center justify-center text-brand-600 text-2xl font-bold mb-4">
						{d.name[0]}
					</div>
					<h3 class="text-lg font-bold text-slate-900">{d.name}</h3>
					<p class="text-sm text-brand-600 font-medium mb-3">{d.role}</p>
					<p class="text-sm text-slate-500 leading-relaxed">{d.bio}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 mb-4">Visit Our Office</h2>
		<p class="text-slate-500 mb-8">{site.address}</p>
		<div class="flex flex-col sm:flex-row justify-center gap-4">
			<a href="tel:{site.phone}" class="inline-flex items-center px-6 py-3 text-sm font-semibold bg-white border border-slate-200 text-slate-700 rounded-lg hover:shadow-md transition-shadow">📞 {site.phone}</a>
			<a href="mailto:{site.email}" class="inline-flex items-center px-6 py-3 text-sm font-semibold bg-white border border-slate-200 text-slate-700 rounded-lg hover:shadow-md transition-shadow">✉️ {site.email}</a>
		</div>
	</div>
</section>
