<script lang="ts">
	import { countries } from '$lib/site';

	const steps = [
		{ num: '01', title: 'Free Profile Assessment', desc: 'Our experts evaluate your academics, goals, and preferences to find the best options.' },
		{ num: '02', title: 'University & Course Selection', desc: 'Shortlist programs matching your profile from our partner institutions worldwide.' },
		{ num: '03', title: 'Application & SOP Support', desc: 'We craft strong applications with compelling statements of purpose and documentation.' },
		{ num: '04', title: 'Visa Filing & Pre-Departure', desc: 'Complete visa application support and guidance until you reach your destination.' }
	];
</script>

<svelte:head><title>Study Abroad — Griffin Immigration</title></svelte:head>

<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">Study Abroad</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">Pursue world-class education in top destinations. We guide you from university selection to visa approval.</p>
	</div>
</section>

<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each countries as c}
				<a href="/study-abroad/{c.slug}" class="group block p-6 rounded-xl border border-slate-200 hover:border-brand-300 hover:shadow-lg transition-all bg-white">
					<img src="https://flagcdn.com/w80/{c.flagCode}.png" alt="{c.name} flag" class="w-12 h-auto rounded shadow-sm mb-4" />
					<h2 class="text-lg font-semibold text-slate-900 group-hover:text-brand-600 transition-colors">{c.name}</h2>
					<p class="mt-2 text-sm text-slate-500">{c.description}</p>
					<div class="mt-4 flex flex-wrap gap-2">
						{#each c.features.slice(0, 3) as f}
							<span class="text-xs px-2.5 py-1 rounded-full bg-slate-100 text-slate-600">{f}</span>
						{/each}
					</div>
				</a>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-12">How It Works</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each steps as step}
				<div class="text-center p-5">
					<div class="w-12 h-12 mx-auto rounded-full bg-brand-100 text-brand-700 flex items-center justify-center font-bold text-lg mb-4">{step.num}</div>
					<h3 class="font-semibold text-slate-900 mb-2">{step.title}</h3>
					<p class="text-sm text-slate-500 leading-relaxed">{step.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-brand-700">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-2xl md:text-3xl font-bold text-white mb-4">Not Sure Where to Study?</h2>
		<p class="text-brand-200 text-lg max-w-xl mx-auto mb-8">Our counselors will help you find the perfect country and program based on your profile.</p>
		<a href="/contact" class="inline-flex items-center px-8 py-4 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">Get Free Counseling</a>
	</div>
</section>
