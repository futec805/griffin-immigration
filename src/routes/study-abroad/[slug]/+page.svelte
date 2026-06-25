<script lang="ts">
	import { countries, site } from '$lib/site';
	import { page } from '$app/stores';

	let country = $derived(countries.find(c => c.slug === $page.params.slug));

	const allInfo: Record<string, {
		edu: { title: string; items: string[] };
		benefits: string[];
		programs: { name: string; desc: string }[];
	}> = {
		canada: { edu: { title: 'Education System', items: ['Top-ranked public universities (UofT, UBC, McGill)', 'Affordable diploma & degree programs', 'Co-op programs with paid internships', '3-year Post-Graduation Work Permit', 'Clear PR pathway through Express Entry'] }, benefits: ['Express Entry points for Canadian education', 'Spouse can work full-time on open work permit', 'Free healthcare in most provinces', 'Pathway to citizenship in 3-5 years', 'Multicultural, safe, and welcoming society'], programs: [{ name: 'Study Permit (SDS)', desc: 'Fast-track study permit processing for eligible Indian students with IELTS 6.0+ in each band.' }, { name: 'Post-Graduation Work Permit', desc: 'Work in Canada for up to 3 years after graduation — gain valuable Canadian work experience.' }, { name: 'Express Entry — Canadian Experience Class', desc: 'Use your Canadian education and work experience to apply for permanent residency.' }, { name: 'Provincial Nominee Program (PNP)', desc: 'Many provinces have dedicated streams for international graduates.' }] },
		australia: { edu: { title: 'Education System', items: ['Group of Eight prestigious universities', 'Wide range of vocational & technical courses', 'Strong research infrastructure', 'Post-study work rights up to 4 years', 'Regional sponsorship options for PR'] }, benefits: ['Temporary Graduate visa (subclass 485)', 'Points for Australian qualifications in PR', 'High minimum wages for part-time work', 'Excellent quality of life and climate', 'Strong Indian diaspora community'], programs: [{ name: 'Student Visa (Subclass 500)', desc: 'Study full-time at an Australian institution with work rights up to 48 hours per fortnight.' }, { name: 'Skilled Independent Visa (Subclass 189)', desc: 'Points-based PR for graduates with skills in demand on the Skilled Occupation List.' }, { name: 'Skilled Nominated Visa (Subclass 190)', desc: 'State-nominated PR pathway — many states prioritize international graduates.' }, { name: 'Temporary Graduate Visa (Subclass 485)', desc: 'Stay and work in Australia for 2-4 years after completing your studies.' }] },
		czech: { edu: { title: 'Education System', items: ['Tuition-free Czech-taught programs at public universities', 'English-taught programs with affordable fees', 'Recognized degrees under Bologna Process', 'Central European hub for tech & engineering', 'EU member state — Schengen area access'] }, benefits: ['Affordable living costs in Europe (€400-700/month)', '9-month job search visa after graduation', 'Access to entire EU job market', 'Rich culture, history, and central location', 'Growing tech and automotive industries'], programs: [{ name: 'Student Visa (Long-term Residence)', desc: 'Study at Czech universities with the right to work part-time during your studies.' }, { name: 'Job Search Visa', desc: '9-month visa to seek employment after graduation — bridge to work permit and EU Blue Card.' }, { name: 'EU Blue Card', desc: 'For highly skilled graduates — work and live anywhere in the European Union.' }, { name: 'Employee Card', desc: 'Dual work-and-residence permit for non-EU graduates who find employment in Czech Republic.' }] },
		uk: { edu: { title: 'Education System', items: ['Oxford, Cambridge & Russell Group universities', '1-year master\'s programs (shorter than most countries)', 'World-leading research output', 'Graduate Route: 2-year post-study work visa', 'Diverse international student community'] }, benefits: ['Graduate Route visa — 2 years (3 for PhD)', 'Skilled Worker visa pathway after studies', 'Free healthcare through NHS surcharge', 'Global recognition of UK qualifications', 'Rich academic heritage and culture'], programs: [{ name: 'Student Visa (Tier 4)', desc: 'Study at a licensed UK institution with permitted work hours during term time.' }, { name: 'Graduate Route', desc: 'Stay and work in the UK for 2 years (3 years for PhD) after completing your degree.' }, { name: 'Skilled Worker Visa', desc: 'Transition from Graduate Route to a sponsored work visa leading to indefinite leave to remain.' }, { name: 'Innovator Founder Visa', desc: 'For graduates with an innovative business idea — start your venture in the UK.' }] },
		germany: { edu: { title: 'Education System', items: ['Tuition-free at most public universities (minimal semester fees)', 'Strong engineering, automotive & tech focus', 'DAAD scholarships for international students', '18-month job seeker visa after graduation', 'EU Blue Card for skilled graduates'] }, benefits: ['Free/very low tuition at public universities', '18-month job seeker visa after graduation', 'EU Blue Card — work anywhere in Europe', 'Strong economy with high demand for engineers & IT', 'Excellent quality of life and infrastructure'], programs: [{ name: 'Student Visa', desc: 'Study at German universities with the right to work 120 full days or 240 half days per year.' }, { name: 'Job Seeker Visa', desc: '18-month visa to find employment matching your qualifications after graduation.' }, { name: 'EU Blue Card', desc: 'Fast-track work and residence permit for graduates earning above the salary threshold.' }, { name: 'Skilled Workers Act', desc: 'Simplified immigration for qualified professionals — Germany needs skilled talent.' }] },
		usa: { edu: { title: 'Education System', items: ['Ivy League & top-tier research universities', 'Flexible credit-based education system', 'STEM OPT extension — 3 years total work authorization', 'World\'s largest economy & job market', 'Diverse campus life & networking opportunities'] }, benefits: ['OPT: 1-year work authorization after graduation', 'STEM OPT extension: additional 2 years (3 total)', 'H-1B visa pathway for skilled workers', 'Access to global companies (FAANG, Fortune 500)', 'World-leading research and innovation ecosystem'], programs: [{ name: 'F-1 Student Visa', desc: 'The primary study visa for international students at US universities and colleges.' }, { name: 'Optional Practical Training (OPT)', desc: 'Work in your field of study for up to 12 months — STEM graduates get 36 months total.' }, { name: 'H-1B Specialty Occupation Visa', desc: 'Employer-sponsored work visa — the main pathway from student to worker status.' }, { name: 'EB-2 / EB-3 Green Card', desc: 'Employment-based permanent residency for professionals with advanced degrees or exceptional ability.' }] }
	};
</script>

<svelte:head><title>{country?.name || ''} Study Visa — Griffin Immigration</title></svelte:head>

{#if country}
	{@const info = allInfo[country.slug]}

	<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<a href="/study-abroad" class="text-brand-300 hover:text-white text-sm mb-6 inline-flex items-center gap-1">
				← Back to Study Abroad
			</a>
			<div class="flex items-center gap-4 mt-2">
				<img src="https://flagcdn.com/w80/{country.flagCode}.png" alt="{country.name} flag" class="w-14 h-auto rounded shadow-sm" />
				<div>
					<h1 class="text-3xl md:text-5xl font-extrabold text-white">Study in {country.name}</h1>
					<p class="mt-3 text-lg text-slate-300 max-w-2xl">{country.description}</p>
				</div>
			</div>
		</div>
	</section>

	<section class="py-16 bg-white">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
				<div>
					<h2 class="text-2xl font-bold text-slate-900 mb-6">{info.edu.title}</h2>
					<ul class="space-y-3">
						{#each info.edu.items as item}
							<li class="flex items-start gap-3 text-sm text-slate-600">
								<span class="text-brand-500 mt-0.5 shrink-0">✓</span>
								{item}
							</li>
						{/each}
					</ul>
				</div>
				<div>
					<h2 class="text-2xl font-bold text-slate-900 mb-6">Key Benefits</h2>
					<ul class="space-y-3">
						{#each info.benefits as b}
							<li class="flex items-start gap-3 text-sm text-slate-600">
								<span class="text-accent-500 mt-0.5 shrink-0">✦</span>
								{b}
							</li>
						{/each}
					</ul>
				</div>
			</div>
		</div>
	</section>

	<section class="py-16 bg-slate-50">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<h2 class="text-2xl font-bold text-slate-900 text-center mb-10">Visa Programs for {country.name}</h2>
			<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
				{#each info.programs as prog}
					<div class="p-6 rounded-xl bg-white border border-slate-200 hover:shadow-md transition-shadow">
						<h3 class="font-semibold text-slate-900 mb-2">{prog.name}</h3>
						<p class="text-sm text-slate-500 leading-relaxed">{prog.desc}</p>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<section class="py-16 bg-brand-700">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
			<h2 class="text-2xl md:text-3xl font-bold text-white mb-4">Want to Study in {country.name}?</h2>
			<p class="text-brand-200 text-lg max-w-xl mx-auto mb-8">Get a free profile assessment and personalized guidance from our expert counselors.</p>
			<a href="/contact" class="inline-flex items-center px-8 py-4 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">Start Free Assessment</a>
		</div>
	</section>
{:else}
	<section class="pt-24 pb-16 text-center">
		<h1 class="text-2xl font-bold text-slate-900">Country not found</h1>
		<a href="/study-abroad" class="mt-4 inline-block text-brand-600 hover:underline">← Back</a>
	</section>
{/if}
