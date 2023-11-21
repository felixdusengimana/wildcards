<script>
	import { page } from '$app/stores';
</script>

<header class="py-3 px-5 flex items-center justify-between bg-[#ccff00]">
	<div>
		<a href="/" class="text-black uppercase font-bold"> wildcards </a>
	</div>

	<nav>
		<ul class="flex gap-3">
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/" class="text-black font-medium">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/#about' ? 'page' : undefined}>
				<a class="text-black font-medium" href="/#about">About</a>
			</li>
			<li aria-current={$page.url.pathname === '/#team' ? 'page' : undefined}>
				<a class="text-black font-medium" href="/#team">Team</a>
			</li>

			<li aria-current={$page.url.pathname.startsWith('/#solution') ? 'page' : undefined}>
				<a class="text-black font-medium" href="/#solution">Solution</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/#challenges') ? 'page' : undefined}>
				<a class="text-black font-medium" href="/#challenges">ELab Challenges</a>
			</li>
		</ul>
	</nav>

	<ul class="flex items-center gap-3">
		<!-- <li>
			<a class="text-black font-medium" href="/login">Log in</a>
		</li>
		<li><button class="bg-white py-2 px-4 rounded-md">Get Started</button></li> -->
	</ul>
</header>
