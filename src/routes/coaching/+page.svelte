<script lang="ts">
	import { coachingFeatures } from '$lib/site';

	const ieltsModules = [
		{ name: 'Listening', desc: '40 questions, 30 minutes. Practice with authentic recordings and targeted exercises.' },
		{ name: 'Reading', desc: '40 questions, 60 minutes. Master skimming, scanning, and comprehension strategies.' },
		{ name: 'Writing', desc: '2 tasks, 60 minutes. Learn essay structures, data interpretation, and letter writing.' },
		{ name: 'Speaking', desc: '3 parts, 11-14 minutes. Mock interviews with detailed pronunciation and fluency feedback.' }
	];

	const pteSections = [
		{ name: 'Speaking & Writing', desc: '54-67 minutes. Personal introduction, read aloud, repeat sentence, describe image, essay writing.' },
		{ name: 'Reading', desc: '29-30 minutes. Fill in the blanks, reorder paragraphs, multiple choice — fully computer-based.' },
		{ name: 'Listening', desc: '30-43 minutes. Summarize spoken text, fill blanks, highlight correct summary, write from dictation.' }
	];

	const batches = [
		{ time: 'Morning', hours: '7:00 AM – 9:00 AM', days: 'Mon – Sat' },
		{ time: 'Evening', hours: '4:00 PM – 6:00 PM', days: 'Mon – Sat' },
		{ time: 'Weekend', hours: '10:00 AM – 2:00 PM', days: 'Sat – Sun' }
	];
</script>

<svelte:head><title>IELTS & PTE Coaching — Griffin Immigration</title></svelte:head>

<section class="bg-gradient-to-br from-slate-900 to-brand-900 pt-20 pb-12 md:pt-24 md:pb-16 text-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h1 class="text-3xl md:text-5xl font-extrabold text-white">IELTS & PTE Coaching</h1>
		<p class="mt-4 text-lg text-slate-300 max-w-2xl">In-house exam preparation with experienced trainers. Achieve your target score with our proven methodology.</p>
	</div>
</section>

<!-- ===== CLASSROOM ===== -->
<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-10 items-center">
			<div class="rounded-2xl overflow-hidden shadow-lg border border-slate-200">
				<img src="/classroom.jpg" alt="Griffin Immigration Classroom — IELTS & PTE Coaching" class="w-full h-80 object-cover" />
			</div>
			<div>
				<h2 class="text-2xl md:text-3xl font-bold text-slate-900 mb-4">Learn in a Space Built for Success</h2>
				<p class="text-slate-600 leading-relaxed mb-4">
					Our classroom isn't just four walls — it's where ambitions take shape. Equipped with modern teaching aids, comfortable seating, and a focused learning environment, every corner of our Sonipat center is designed to help you concentrate, prepare, and excel.
				</p>
				<p class="text-slate-600 leading-relaxed mb-6">
					Small batch sizes mean you get the personal attention you deserve. Our trainers know you by name, understand your weak spots, and work with you one-on-one until you cross that target band score. Hundreds of students have walked through these doors with a dream — and walked out with a visa.
				</p>
				<div class="flex flex-wrap gap-4">
					<div class="flex items-center gap-2 text-sm text-slate-700"><span class="w-2 h-2 rounded-full bg-brand-500"></span> Air-conditioned classroom</div>
					<div class="flex items-center gap-2 text-sm text-slate-700"><span class="w-2 h-2 rounded-full bg-brand-500"></span> Smart board for visual learning</div>
					<div class="flex items-center gap-2 text-sm text-slate-700"><span class="w-2 h-2 rounded-full bg-brand-500"></span> Weekly mock tests on-site</div>
					<div class="flex items-center gap-2 text-sm text-slate-700"><span class="w-2 h-2 rounded-full bg-brand-500"></span> Individual doubt-clearing sessions</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
			<!-- IELTS -->
			<div class="rounded-2xl border border-brand-100 bg-brand-50/40 p-6 md:p-8 flex flex-col">
				<h2 class="text-2xl font-bold text-slate-900 mb-1">IELTS Training</h2>
				<p class="text-slate-500 text-sm mb-6">International English Language Testing System — accepted by 11,000+ institutions worldwide.</p>
				<div class="space-y-3 flex-1">
					{#each ieltsModules as m}
						<div class="p-4 rounded-xl bg-white border border-brand-100/60">
							<h3 class="font-semibold text-slate-900 text-sm">{m.name}</h3>
							<p class="text-xs text-slate-500 mt-1">{m.desc}</p>
						</div>
					{/each}
				</div>
				<div class="mt-6 grid grid-cols-3 gap-3">
					<div class="text-center p-3 rounded-xl bg-white border border-brand-100/60"><div class="text-xl font-bold text-brand-600">7.5+</div><div class="text-xs text-slate-500">Avg Band</div></div>
					<div class="text-center p-3 rounded-xl bg-white border border-brand-100/60"><div class="text-xl font-bold text-brand-600">200+</div><div class="text-xs text-slate-500">Students</div></div>
					<div class="text-center p-3 rounded-xl bg-white border border-brand-100/60"><div class="text-xl font-bold text-brand-600">4</div><div class="text-xs text-slate-500">Mock Tests/mo</div></div>
				</div>
			</div>

			<!-- PTE -->
			<div class="rounded-2xl border border-accent-100 bg-accent-50/40 p-6 md:p-8 flex flex-col">
				<h2 class="text-2xl font-bold text-slate-900 mb-1">PTE Training</h2>
				<p class="text-slate-500 text-sm mb-6">Pearson Test of English — computer-based exam preferred by universities in Australia, UK, and New Zealand.</p>
				<div class="space-y-3 flex-1">
					{#each pteSections as s}
						<div class="p-4 rounded-xl bg-white border border-accent-100/60">
							<h3 class="font-semibold text-slate-900 text-sm">{s.name}</h3>
							<p class="text-xs text-slate-500 mt-1">{s.desc}</p>
						</div>
					{/each}
				</div>
				<div class="mt-6 grid grid-cols-3 gap-3">
					<div class="text-center p-3 rounded-xl bg-white border border-accent-100/60"><div class="text-xl font-bold text-accent-600">79+</div><div class="text-xs text-slate-500">Avg Score</div></div>
					<div class="text-center p-3 rounded-xl bg-white border border-accent-100/60"><div class="text-xl font-bold text-accent-600">150+</div><div class="text-xs text-slate-500">Students</div></div>
					<div class="text-center p-3 rounded-xl bg-white border border-accent-100/60"><div class="text-xl font-bold text-accent-600">4</div><div class="text-xs text-slate-500">Tests/mo</div></div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="py-16 bg-slate-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-4">Why Our Coaching Works</h2>
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 mt-10">
			{#each coachingFeatures as f}
				<div class="p-6 rounded-xl bg-white border border-slate-200">
					<div class="text-3xl mb-3">{f.icon}</div>
					<h3 class="font-semibold text-slate-900 mb-2">{f.title}</h3>
					<p class="text-sm text-slate-500 leading-relaxed">{f.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-white">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<h2 class="text-2xl md:text-3xl font-bold text-slate-900 text-center mb-10">Batch Timings</h2>
		<div class="grid grid-cols-1 sm:grid-cols-3 gap-6 max-w-3xl mx-auto">
			{#each batches as batch}
				<div class="p-6 rounded-xl border border-slate-200 text-center bg-white">
					<div class="text-lg font-bold text-brand-600 mb-1">{batch.time}</div>
					<div class="text-sm text-slate-500">{batch.hours}</div>
					<div class="text-xs text-slate-400 mt-1">{batch.days}</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-16 bg-brand-700">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-2xl md:text-3xl font-bold text-white mb-4">Enroll in a Batch Today</h2>
		<p class="text-brand-200 text-lg max-w-xl mx-auto mb-8">Limited seats per batch. Book your slot now and start your IELTS/PTE preparation.</p>
		<a href="/contact" class="inline-flex items-center px-8 py-4 text-base font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-lg shadow-accent-500/25">Enroll Now</a>
	</div>
</section>
