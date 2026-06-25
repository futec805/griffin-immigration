<script lang="ts">
	import { countries, services, testimonials, stats, site } from '$lib/site';
</script>

<svelte:head>
	<title>{site.name} — Immigration & Study Abroad Consultants</title>
	<meta name="description" content="Expert immigration consultancy for Canada, Australia, UK, Germany, USA, Czech Republic. Student visas, PR, IELTS & PTE coaching in Sonipat." />
</svelte:head>

<!-- ===== HERO ===== -->
<section class="relative bg-gradient-to-br from-slate-900 via-slate-800 to-brand-900 overflow-hidden">
	<div class="absolute inset-0 opacity-10">
		<div class="absolute -top-40 -right-40 w-96 h-96 rounded-full bg-brand-400 blur-3xl"></div>
		<div class="absolute -bottom-20 -left-20 w-80 h-80 rounded-full bg-accent-400 blur-3xl"></div>
	</div>
	<div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-12 pb-20 md:pt-20 md:pb-28">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">
			<!-- Left: Text -->
			<div>
				<div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-white/10 border border-white/10 text-white/80 text-xs font-medium mb-4">
					<span class="w-1.5 h-1.5 rounded-full bg-accent-400"></span>
					India's Trusted Immigration Partner
				</div>
				<h1 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl font-black leading-[1.15] mb-3 pb-2" style="background: linear-gradient(135deg, #fbbf24 0%, #f59e0b 15%, #e67e22 30%, #f0f9ff 50%, #60a5fa 70%, #3b82f6 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; filter: drop-shadow(0 6px 30px rgba(37, 99, 235, 0.35));">
					Griffin<br class="sm:hidden" /> Immigration
				</h1>
				<div class="flex items-center gap-3 mb-1">
					<div class="h-0.5 flex-1 bg-gradient-to-r from-transparent via-accent-400 to-transparent max-w-12 rounded-full"></div>
					<p class="text-base sm:text-lg font-bold tracking-[0.25em] text-accent-400 uppercase">Your Global Future Starts Here</p>
					<div class="h-0.5 flex-1 bg-gradient-to-r from-transparent via-accent-400 to-transparent max-w-12 rounded-full"></div>
				</div>
				<div class="flex items-center gap-2 -mt-0.5">
					<div class="h-0.5 w-12 bg-gradient-to-r from-transparent via-brand-400 to-brand-500 rounded-full"></div>
					<div class="h-0.5 w-6 bg-gradient-to-r from-brand-400 to-accent-400 rounded-full"></div>
					<div class="h-0.5 w-3 bg-accent-400 rounded-full"></div>
				</div>
				<p class="mt-6 text-lg text-slate-300 max-w-xl leading-relaxed">
					Expert guidance for studying, working, and settling abroad. From university selection to visa approval — we handle it all.
				</p>
				<div class="mt-6 flex flex-wrap gap-x-6 gap-y-2 text-sm text-slate-400">
					<div class="flex items-center gap-2"><span class="text-accent-400">▸</span> Student Visas — 6+ Countries</div>
					<div class="flex items-center gap-2"><span class="text-accent-400">▸</span> Work Permits & PR Pathways</div>
					<div class="flex items-center gap-2"><span class="text-accent-400">▸</span> In-House IELTS & PTE Coaching</div>
					<div class="flex items-center gap-2"><span class="text-accent-400">▸</span> 500+ Successful Visa Approvals</div>
					<div class="flex items-center gap-2"><span class="text-accent-400">▸</span> End-to-End Documentation Support</div>
				</div>
				<div class="mt-8 flex flex-col sm:flex-row gap-4">
					<a href="/contact" class="inline-flex items-center justify-center px-6 py-3.5 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">
						Get Free Assessment
						<svg class="ml-2 w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
					</a>
					<a href="/study-abroad" class="inline-flex items-center justify-center px-6 py-3.5 text-base font-semibold text-white border border-white/20 hover:bg-white/10 rounded-lg transition-colors">
						Explore Countries
					</a>
				</div>

				<!-- Stats row -->
				<div class="mt-12 grid grid-cols-2 sm:grid-cols-4 gap-6">
					{#each stats as stat}
						<div>
							<div class="text-2xl md:text-3xl font-bold text-white">{stat.value}</div>
							<div class="text-sm text-slate-400 mt-1">{stat.label}</div>
						</div>
					{/each}
				</div>
			</div>

			<!-- Right: Image -->
			<div class="hidden lg:block">
				<div class="relative">
					<div class="absolute -inset-4 bg-gradient-to-tr from-accent-500/20 to-brand-500/20 rounded-3xl blur-xl"></div>
					<img
						src="/office.jpg"
						alt="Griffin Immigration — Your trusted partner for study abroad and immigration"
						class="relative rounded-2xl shadow-2xl w-full aspect-[4/3] object-cover border border-white/10"
					/>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- ===== COUNTRIES ===== -->
<section class="py-20 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-14">
			<h2 class="text-3xl md:text-4xl font-bold text-slate-900">Study & Settle Abroad</h2>
			<p class="mt-3 text-slate-500 text-lg max-w-2xl mx-auto">Explore opportunities in top destinations for education, work, and permanent residency.</p>
		</div>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each countries as c}
				<a href="/study-abroad/{c.slug}"
					class="group relative block rounded-2xl overflow-hidden h-72 bg-cover bg-center shadow-md hover:shadow-xl hover:-translate-y-1 transition-all duration-300"
					style="background-image: url('{c.bgImage}')"
				>
					<!-- Faded overlay — photo is subtle, text pops -->
					<div class="absolute inset-0 bg-gradient-to-b from-white/50 via-white/80 to-white/95"></div>
					<!-- Content -->
					<div class="relative h-full p-5 flex flex-col">
						<img src="https://flagcdn.com/w80/{c.flagCode}.png" alt="{c.name} flag" class="w-12 h-auto rounded shadow-sm mb-2" />
						<h3 class="text-2xl font-extrabold {c.nameColor} mb-1.5 drop-shadow-sm">{c.name}</h3>
						<p class="text-sm font-medium text-slate-700 leading-snug mb-3">{c.description}</p>
						<div class="mt-auto flex flex-wrap gap-1.5">
							{#each c.features.slice(0, 3) as f}
								<span class="text-xs px-2.5 py-1 rounded-full bg-white/90 text-slate-700 font-medium shadow-sm border border-white">{f}</span>
							{/each}
						</div>
					</div>
				</a>
			{/each}
		</div>
	</div>
</section>

<!-- ===== OFFICE PHOTOS ===== -->
<section class="py-20 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-12">
			<h2 class="text-3xl md:text-4xl font-bold text-slate-900">Our Office</h2>
			<p class="mt-3 text-slate-500 text-lg">Visit us at our Sonipat office — where your journey begins.</p>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			<div class="rounded-xl overflow-hidden border border-slate-200 shadow-sm">
				<img src="/office.jpg" alt="Griffin Immigration Office" class="w-full h-64 object-cover" />
			</div>
			<div class="rounded-xl overflow-hidden border border-slate-200 shadow-sm">
				<img src="/office-1.jpg" alt="Griffin Immigration Office Interior" class="w-full h-64 object-cover" />
			</div>
		</div>
	</div>
</section>

<!-- ===== SERVICES ===== -->
<section class="py-20 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-14">
			<h2 class="text-3xl md:text-4xl font-bold text-slate-900">Our Services</h2>
			<p class="mt-3 text-slate-500 text-lg max-w-2xl mx-auto">Comprehensive immigration and education support under one roof.</p>
		</div>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each services as svc}
				<div class="p-6 rounded-xl bg-white border border-slate-200 hover:shadow-md transition-shadow">
					<div class="text-3xl mb-4">{svc.icon}</div>
					<h3 class="text-lg font-semibold text-slate-900 mb-2">{svc.title}</h3>
					<p class="text-sm text-slate-500 leading-relaxed">{svc.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- ===== TESTIMONIALS ===== -->
<section class="py-20 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-14">
			<h2 class="text-3xl md:text-4xl font-bold text-slate-900">Success Stories</h2>
			<p class="mt-3 text-slate-500 text-lg max-w-2xl mx-auto">Hear from students and professionals who achieved their dreams with us.</p>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			{#each testimonials as t}
				<div class="p-6 rounded-xl border border-slate-200 bg-white hover:shadow-md transition-shadow">
					<div class="flex gap-1 mb-3">
						{#each Array(t.rating) as _}
							<span class="text-amber-400">★</span>
						{/each}
					</div>
					<p class="text-sm text-slate-600 leading-relaxed mb-4">"{t.text}"</p>
					<div class="flex items-center gap-3">
						<div class="w-10 h-10 rounded-full bg-brand-100 flex items-center justify-center text-brand-600 font-bold text-sm">
							{t.name[0]}
						</div>
						<div>
							<div class="text-sm font-semibold text-slate-900">{t.name}</div>
							<div class="text-xs text-slate-400">{t.destination}</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- ===== CTA ===== -->
<section class="py-20 bg-gradient-to-r from-brand-700 to-brand-900">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-white mb-4">Ready to Start Your Journey?</h2>
		<p class="text-brand-200 text-lg max-w-xl mx-auto mb-8">Schedule a free consultation with our immigration experts today.</p>
		<div class="flex flex-col sm:flex-row justify-center gap-4">
			<a href="/contact" class="inline-flex items-center justify-center px-8 py-4 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">
				Get Free Consultation
			</a>
			<a href="tel:+917274080000" class="inline-flex items-center justify-center px-8 py-4 text-base font-semibold text-white border border-white/20 hover:bg-white/10 rounded-lg transition-colors">
				📞 Call Now
			</a>
		</div>
	</div>
</section>
