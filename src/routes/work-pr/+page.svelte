<script lang="ts">
	const programs = [
		{ title: 'Express Entry (Canada)', desc: 'The fastest route to Canadian permanent residency for skilled workers. Based on CRS points — age, education, work experience, and language ability.', features: ['No job offer required for FSW program', 'Processing time: 6-8 months', 'CRS score calculator with live draw predictions', 'Provincial Nominee Program (PNP) integration'] },
		{ title: 'Skilled Migration (Australia)', desc: 'Points-based PR pathways including Subclass 189, 190, and 491 for skilled professionals.', features: ['Skilled Occupation List (SOL) assessment', 'State nomination for extra points', 'Regional visa options (subclass 491)', 'Points test optimization strategy'] },
		{ title: 'Skilled Worker Visa (UK)', desc: 'Work and settle in the UK through employer sponsorship under the points-based system.', features: ['Job matching with licensed sponsors', 'Health & Care Worker visa option', 'Path to Indefinite Leave to Remain', 'Dependent family included'] },
		{ title: 'EU Blue Card (Germany)', desc: 'Work permit for highly qualified non-EU nationals with a university degree and job offer.', features: ['Fast-track permanent residency in 33 months', 'Full access to EU labor market', 'Family reunification included', 'Recognition of Indian qualifications'] }
	];

	const prSteps = [
		{ num: '01', title: 'Eligibility Check', desc: 'Free profile assessment against multiple PR programs across countries.' },
		{ num: '02', title: 'Document Preparation', desc: 'IELTS, ECA, work reference letters, and all documentation handled by our team.' },
		{ num: '03', title: 'Application Filing', desc: 'Complete application preparation and submission with quality review.' },
		{ num: '04', title: 'Post-Submission', desc: 'Follow-up with authorities, medical, biometrics, and landing support.' }
	];
</script>

<svelte:head><title>Work Visa & PR — Griffin Immigration</title></svelte:head>

<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">Work Visa & PR</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">Build your career and secure permanent residency in top global destinations. Expert guidance for skilled workers and professionals.</p>
	</div>
</section>

<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			{#each programs as prog}
				<div class="p-6 rounded-xl border border-slate-200 hover:shadow-lg transition-shadow bg-white">
					<h2 class="text-xl font-bold text-slate-900 mb-3">{prog.title}</h2>
					<p class="text-sm text-slate-500 leading-relaxed mb-4">{prog.desc}</p>
					<ul class="space-y-2">
						{#each prog.features as f}
							<li class="flex items-start gap-2 text-sm text-slate-600">
								<span class="text-brand-500 mt-0.5 shrink-0">✓</span>{f}
							</li>
						{/each}
					</ul>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-12">Our Process</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each prSteps as step}
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
		<h2 class="text-2xl md:text-3xl font-bold text-white mb-4">Check Your PR Eligibility</h2>
		<p class="text-brand-200 text-lg max-w-xl mx-auto mb-8">Find out which PR programs you qualify for — free assessment in 5 minutes.</p>
		<a href="/contact" class="inline-flex items-center px-8 py-4 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">Get Free Assessment</a>
	</div>
</section>
