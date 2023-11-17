<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Welcome to wildcards thinktank</title>
	<meta name="description" content="wildcards showcase what they do best" />
</svelte:head>

<section class="bg-[url('$lib/images/home.jpg')] py-10 bg-cover bg-no-repeat w-full min-h-[1000px]">
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>
		<p class="font-bold max-w-[500px] mx-auto text-center">Join the Education Revolution with Wildcards</p>
	</h1>
</section>

<div>
	<p>How it works</p>
	<h1>Embark on Your Green Journey</h1>
</div>

<style>
	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 100px;
		display: block;
	}
</style>
