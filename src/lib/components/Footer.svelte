<script lang="ts">
	import { site } from '$lib/site';
</script>

<footer class="bg-slate-900 text-slate-300">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-10">
			<!-- Brand -->
			<div>
				<img src="/logo.jpeg" alt="Griffin" class="h-8 w-auto mb-4 brightness-0 invert" />
				<p class="text-sm text-slate-400 leading-relaxed mb-4">
					Your trusted partner for global education and immigration.
				</p>
				<div class="flex items-center gap-3">
					<a href={site.social.instagram} target="_blank" class="text-slate-400 hover:text-white transition-colors" aria-label="Instagram">
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069z"/></svg>
					</a>
				</div>
			</div>

			<!-- Quick Links -->
			<div>
				<h4 class="text-white font-semibold mb-4 text-sm uppercase tracking-wider">Quick Links</h4>
				<ul class="space-y-2.5 text-sm">
					<li><a href="/" class="hover:text-white transition-colors">Home</a></li>
					<li><a href="/study-abroad" class="hover:text-white transition-colors">Study Abroad</a></li>
					<li><a href="/work-pr" class="hover:text-white transition-colors">Work & PR</a></li>
					<li><a href="/coaching" class="hover:text-white transition-colors">IELTS / PTE</a></li>
					<li><a href="/services" class="hover:text-white transition-colors">Our Services</a></li>
				</ul>
			</div>

			<!-- Services -->
			<div>
				<h4 class="text-white font-semibold mb-4 text-sm uppercase tracking-wider">Services</h4>
				<ul class="space-y-2.5 text-sm">
					<li><a href="/study-abroad" class="hover:text-white transition-colors">Student Visa</a></li>
					<li><a href="/work-pr" class="hover:text-white transition-colors">Work Visa & PR</a></li>
					<li><a href="/coaching" class="hover:text-white transition-colors">IELTS Coaching</a></li>
					<li><a href="/coaching" class="hover:text-white transition-colors">PTE Coaching</a></li>
				</ul>
			</div>

			<!-- Contact -->
			<div>
				<h4 class="text-white font-semibold mb-4 text-sm uppercase tracking-wider">Contact</h4>
				<ul class="space-y-2.5 text-sm">
					<li class="flex items-start gap-2">
						<span class="mt-0.5 shrink-0">📍</span>
						<span>{site.address}</span>
					</li>
					<li class="flex items-center gap-2">
						<span>📞</span>
						<a href="tel:{site.phone}" class="hover:text-white transition-colors">{site.phone}</a>
					</li>
					<li class="flex items-center gap-2">
						<span>✉️</span>
						<a href="mailto:{site.email}" class="hover:text-white transition-colors">{site.email}</a>
					</li>
					<li class="flex items-center gap-2">
						<span>🕐</span>
						<span>{site.hours}</span>
					</li>
				</ul>
			</div>
		</div>
	</div>

	<!-- Bottom bar -->
	<div class="border-t border-slate-800">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-5 flex flex-col sm:flex-row justify-between items-center gap-2 text-xs text-slate-500">
			<span>&copy; {new Date().getFullYear()} Griffin Immigration Pvt. Ltd. All rights reserved.</span>
			<span>CIN: U74999HR2022PTC106123</span>
		</div>
	</div>
</footer>
