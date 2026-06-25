<script lang="ts">
	const stories = [
		{ name: 'Rohit Sharma', destination: 'Canada Student Visa — University of Toronto', text: 'Griffin Immigration guided me through every step of my Canada study visa. From university selection to visa approval — everything was smooth and professional. I am now pursuing my Masters at the University of Toronto.', rating: 5 },
		{ name: 'Priya Verma', destination: 'Australia PR — Subclass 190', text: 'Got my Australia PR through their skilled migration program. The team was incredibly knowledgeable and responsive throughout the process. They helped me with skill assessment and state nomination.', rating: 5 },
		{ name: 'Amit Kumar', destination: 'IELTS Coaching — Band 7.5', text: 'Scored 7.5 bands in IELTS thanks to the dedicated coaching at Griffin. The mock tests and personalized feedback made all the difference. The trainers are highly experienced.', rating: 5 },
		{ name: 'Neha Rani', destination: 'UK Student Visa — University of Manchester', text: 'The admission guidance and SOP support was excellent. Got admission to my dream university in the UK. Highly recommended for anyone planning to study abroad.', rating: 5 },
		{ name: 'Vikram Singh', destination: 'Canada Express Entry PR', text: 'Applied for Canada PR through Express Entry with Griffin\'s help. They guided me through ECA, IELTS, and CRS optimization. Got my ITA in just 3 months.', rating: 5 },
		{ name: 'Anjali Gupta', destination: 'Germany Student Visa — TU Munich', text: 'Wanted to study engineering in Germany but was confused about the process. Griffin helped with university shortlisting, application, and visa — all free of cost for public universities.', rating: 5 },
		{ name: 'Sandeep Yadav', destination: 'Australia Student Visa', text: 'Very professional team. They handled my admission and visa process efficiently. Now studying at the University of Melbourne. Thank you Griffin team!', rating: 5 },
		{ name: 'Megha Arora', destination: 'PTE Coaching — Score 85', text: 'The PTE preparation at Griffin was excellent. Small batch sizes meant personal attention. Scored 85 in my first attempt. The mock tests were very helpful.', rating: 5 },
		{ name: 'Rahul Bhatia', destination: 'Czech Republic Student Visa', text: 'Studying in Europe seemed impossible due to costs, but Griffin showed me the Czech Republic option. Affordable tuition, great education, and now I have EU exposure.', rating: 5 },
		{ name: 'Pooja Malik', destination: 'Canada Spouse Open Work Permit', text: 'My husband was studying in Canada and Griffin helped me get my spouse open work permit. The process was seamless and we are now both in Toronto.', rating: 5 }
	];

	const results = [
		{ src: '/success-stories/ielts-1.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-2.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-3.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-4.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-5.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-6.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-7.PNG',    label: 'IELTS' },
		{ src: '/success-stories/ielts-8.PNG',    label: 'IELTS' },
		{ src: '/success-stories/ielts-9.jpeg',  label: 'IELTS' },
		{ src: '/success-stories/ielts-10.jpeg', label: 'IELTS' },
		{ src: '/success-stories/pte-11.jpeg',   label: 'PTE' },
		{ src: '/success-stories/pte-12.jpeg',   label: 'PTE' },
		{ src: '/success-stories/pte-13.PNG',    label: 'PTE' },
		{ src: '/success-stories/pte-14.jpeg',   label: 'PTE' },
		{ src: '/success-stories/pte-15.jpeg',   label: 'PTE' },
		{ src: '/success-stories/pte-16.jpeg',   label: 'PTE' },
		{ src: '/success-stories/pte-17.jpeg',   label: 'PTE' },
	];
</script>

<svelte:head><title>Success Stories — Griffin Immigration</title></svelte:head>

<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">Success Stories</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">Real results from our students. 500+ visas approved and counting.</p>
	</div>
</section>

<!-- ===== SUCCESS HIGHLIGHTS + STUDENT VIDEO ===== -->
<section class="py-16 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-10 items-center">
			<div>
				<h2 class="text-2xl md:text-3xl font-extrabold text-slate-900 mb-6">Proven Results. Real Success.</h2>
				<div class="space-y-4 text-slate-600 leading-relaxed">
					<p>At Griffin Immigration, our track record speaks for itself. We have consistently achieved <strong class="text-brand-600">outstanding IELTS and PTE results</strong> — our students regularly score 7+ bands in IELTS and 79+ in PTE, giving them a competitive edge in visa applications and university admissions worldwide.</p>
					<p>Our students have <strong class="text-brand-600">obtained visas for Canada, Australia, the UK, Germany, the USA, and the Czech Republic</strong>. Whether it's a study visa or a work permit, our near-perfect success rate is built on meticulous documentation, honest counseling, and years of experience navigating complex immigration systems.</p>
					<p>Almost every student who walks through our doors gets their visa approved. We don't just coach — <strong class="text-brand-600">we guide, support, and fight for your dream</strong> until you're holding that approval letter in your hands.</p>
					<p>Our alumni are now studying at the University of Toronto, University of Manchester, TU Munich, University of Melbourne, and many more. Some have secured PR in Canada and Australia through Express Entry and Subclass 190. <strong class="text-accent-600">Your name could be next.</strong></p>
				</div>
			</div>
			<div>
				<div class="rounded-2xl overflow-hidden shadow-lg border border-slate-200 bg-black">
					<video controls poster="/office.jpg" class="w-full aspect-video object-cover" preload="metadata">
						<source src="/student-review.mp4" type="video/mp4" />
						Your browser does not support the video tag.
					</video>
				</div>
				<p class="text-center text-sm text-slate-500 mt-3">Hear from our students — real experiences, real journeys</p>
			</div>
		</div>
	</div>
</section>

<!-- ===== IELTS & PTE SCORECARDS ===== -->
<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-10">
			<h2 class="text-2xl md:text-3xl font-extrabold text-slate-900">IELTS & PTE Results</h2>
			<p class="mt-2 text-slate-500 max-w-xl mx-auto">Real scorecards from our students — 7+ bands in IELTS and high scores in PTE, opening doors to top universities and PR pathways worldwide.</p>
		</div>
		<div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-4">
			{#each results as r}
				<div class="group rounded-xl overflow-hidden border border-slate-200 bg-slate-50 hover:shadow-lg transition-shadow relative">
					<div class="absolute top-2 left-2 z-10">
						<span class="px-2 py-0.5 text-[10px] font-bold rounded-full {r.label === 'IELTS' ? 'bg-brand-500 text-white' : 'bg-accent-500 text-white'}">{r.label}</span>
					</div>
					<div class="aspect-[3/4] overflow-hidden">
						<img src={r.src} alt="{r.label} Scorecard" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300" loading="lazy" />
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- ===== TESTIMONIALS ===== -->
<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-10">
			<h2 class="text-2xl md:text-3xl font-extrabold text-slate-900">What Our Students Say</h2>
			<p class="mt-2 text-slate-500">Hear from students and professionals who trusted Griffin Immigration with their dreams.</p>
		</div>
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			{#each stories as story}
				<div class="p-6 rounded-xl border border-slate-200 bg-white hover:shadow-md transition-shadow">
					<div class="flex gap-0.5 mb-3">
						{#each Array(story.rating) as _}
							<span class="text-amber-400 text-sm">★</span>
						{/each}
					</div>
					<p class="text-sm text-slate-600 leading-relaxed mb-4">"{story.text}"</p>
					<div class="flex items-center gap-3 border-t border-slate-100 pt-4">
						<div class="w-10 h-10 rounded-full bg-brand-100 flex items-center justify-center text-brand-600 font-bold text-sm">
							{story.name[0]}
						</div>
						<div>
							<div class="text-sm font-semibold text-slate-900">{story.name}</div>
							<div class="text-xs text-slate-400">{story.destination}</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-brand-700">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-2xl md:text-3xl font-bold text-white mb-4">Be Our Next Success Story</h2>
		<p class="text-brand-200 text-lg max-w-xl mx-auto mb-8">Join 500+ students and professionals who achieved their dreams with Griffin Immigration.</p>
		<a href="/contact" class="inline-flex items-center px-8 py-4 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">Start Your Journey</a>
	</div>
</section>
