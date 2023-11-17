<script>
	import Header from './components/Header.svelte';
	import './styles.css';
</script>

<div class="">
	
	<main class="relative" >
		<div class="fixed top-0 w-full h-fit z-50"><Header /></div>
		<div>
			<slot />
		</div>
	</main>

	<footer class="text-3xl text-red-500 font-bold underline">
		wildcards think-tank
	</footer>
</div>