<script lang="ts">
	let { pathname = '' } = $props();
	let mobileOpen = $state(false);

	const links = [
		{ label: 'Home', href: '/' },
		{ label: 'Our Services', href: '/services' },
		{ label: 'IELTS / PTE', href: '/coaching' },
		{ label: 'Study Abroad', href: '/study-abroad' },
		{ label: 'Work & PR', href: '/work-pr' },
		{ label: 'About Us', href: '/about' },
		{ label: 'Success Stories', href: '/success' },
		{ label: 'Contact', href: '/contact' }
	];

	function active(href: string) {
		if (href === '/') return pathname === '/';
		return pathname.startsWith(href);
	}
</script>

<header class="sticky top-0 z-50 bg-white/95 backdrop-blur border-b border-slate-200">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex items-center justify-between h-16">
			<!-- Logo -->
			<a href="/" class="flex items-center gap-2 shrink-0">
				<img src="/logo.jpeg" alt="Griffin Immigration" class="h-10 w-auto" />
			</a>

			<!-- Desktop nav -->
			<nav class="hidden lg:flex items-center gap-1">
				{#each links as link}
					<a
						href={link.href}
						class="px-3 py-2 text-sm font-medium rounded-md transition-colors
							{active(link.href)
							? 'text-brand-600 bg-brand-50'
							: 'text-slate-600 hover:text-slate-900 hover:bg-slate-50'}"
					>
						{link.label}
					</a>
				{/each}
			</nav>

			<!-- CTA -->
			<div class="hidden lg:flex items-center gap-3">
				<a href="https://wa.me/917274080000" target="_blank" class="text-sm font-medium text-slate-600 hover:text-brand-600 transition-colors">
					+91 7274080000
				</a>
				<a href="/contact" class="inline-flex items-center px-4 py-2 text-sm font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg transition-colors shadow-sm">
					Free Assessment
				</a>
			</div>

			<!-- Mobile hamburger -->
			<button class="lg:hidden p-2 text-slate-600" onclick={() => mobileOpen = !mobileOpen} aria-label="Menu">
				<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					{#if mobileOpen}
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
					{:else}
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
					{/if}
				</svg>
			</button>
		</div>
	</div>

	<!-- Mobile menu -->
	{#if mobileOpen}
		<div class="lg:hidden border-t border-slate-100 bg-white">
			<nav class="px-4 py-3 space-y-1">
				{#each links as link}
					<a
						href={link.href}
						class="block px-3 py-2.5 rounded-md text-sm font-medium transition-colors
							{active(link.href)
							? 'text-brand-600 bg-brand-50'
							: 'text-slate-600 hover:text-slate-900 hover:bg-slate-50'}"
					>
						{link.label}
					</a>
				{/each}
				<div class="pt-3 border-t border-slate-100">
					<a href="/contact" class="block w-full text-center px-4 py-2.5 text-sm font-semibold text-white bg-accent-500 hover:bg-accent-600 rounded-lg shadow-sm">
						Free Assessment
					</a>
				</div>
			</nav>
		</div>
	{/if}
</header>
