<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	const team = [{
		id: 1,
		name: 'Felix Dusengimana',
		socials: [{
			name: 'twitter',
			link: 'https://twitter.com/felixdusengiman'
		}, {
			name: 'linkedin',
			link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
		}],
		role: 'Co-Founder & CTO',
		avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
		insp_quote: '“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
	}, {
		id: 2,
		name: 'Erneste Ntezirizaza',
		socials: [{
			name: 'twitter',
			link: 'https://twitter.com/felixdusengiman'
		}, {
			name: 'linkedin',
			link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
		}],
		role: 'Co-Founder & CEO',
		avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
		insp_quote: '“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
	}, {
		id: 3,
		name: 'Irakoze Hortance',
		socials: [{
			name: 'twitter',
			link: 'https://twitter.com/felixdusengiman'
		}, {
			name: 'linkedin',
			link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
		}],
		role: 'Co-Founder & COO',
		avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
		insp_quote: '“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
	},]
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

<section id="about">
	<div class="max-w-[500px] mx-auto">
		<h1 class="text-center">About Us</h1>
		<p class="text-center">
			We are a team of passionate individuals who believe that education is the key to a better future. We
			are committed to providing the best education to everyone, regardless of their background and
			ability.
		</p>
	</div>
</section>

<section id="team" class="mt-40">
	<div class="max-w-[500px] mx-auto">
		<h1 class="text-center">Our Team</h1>
		<p class="text-center">
			We are a team of passionate individuals who believe that education is the key to a better future. We
			are committed to providing the best education to everyone, regardless of their background and
			ability.
		</p>
	</div>
	<div class="grid grid-cols-3 gap-4 max-w-[1200px] mx-auto mt-4">
		{#each team as item, index (item.id)}
		<div class="bg-white border shadow p-4">
         <p class="text-center font-bold">{item.name}</p>
		 <p class="text-center">{item.role}</p>
		 <div class="flex justify-center gap-2">
			{#each item.socials as social}
			<a href={social.link} target="_blank" rel="noopener noreferrer">
					<img src={`https://img.icons8.com/${social.name}/000000/${social.name}`} alt={social.name} />
				</a>
			{/each}
	      </div>
		  
		  <article class="mt-4">
			  <p class="text-center">{item.insp_quote}</p>
		  </article>
		</div>
		{/each}
	</div>
</section>

<section id="solution" class="mt-40">
	<div class="max-w-[500px] mx-auto">
		<h1 class="text-center">Our Solution</h1>
		<p class="text-center">
			We are a team of passionate individuals who believe that education is the key to a better future. We
			are committed to providing the best education to everyone, regardless of their background and
			ability.
		</p>
	</div>
</section>
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
