<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import felix from '$lib/images/felix.png';
	import ELabChallenges from './components/ELabChallenges.svelte';

	const team = [
		{
			id: 2,
			name: 'Erneste Ntezirizaza',
			socials: [
				{
					name: 'twitter',
					link: 'https://twitter.com/felixdusengiman'
				},
				{
					name: 'linkedin',
					link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
				}
			],
			role: 'Co-Founder & CEO',
			avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
			insp_quote:
				'“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
		},
		{
			id: 3,
			name: 'Irakoze Hortance',
			socials: [
				{
					name: 'twitter',
					link: 'https://twitter.com/felixdusengiman'
				},
				{
					name: 'linkedin',
					link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
				}
			],
			role: 'Co-Founder & COO',
			avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
			insp_quote:
				'“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
		},
		{
			id: 4,
			name: 'Irakoze Hortance',
			socials: [
				{
					name: 'twitter',
					link: 'https://twitter.com/felixdusengiman'
				},
				{
					name: 'linkedin',
					link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
				}
			],
			role: 'Co-Founder & COO',
			avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
			insp_quote:
				'“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
		},
		{
			id: 5,
			name: 'Irakoze Hortance',
			socials: [
				{
					name: 'twitter',
					link: 'https://twitter.com/felixdusengiman'
				},
				{
					name: 'linkedin',
					link: 'https://www.linkedin.com/in/felix-dusengimana-0b0b0b1b0/'
				},
				{
					name: 'instagram',
					link: ''
				},
				{
					name: 'facebook',
					link: ''
				}
			],
			role: 'Co-Founder & COO',
			avatar: 'https://avatars.githubusercontent.com/u/29729380?v=4',
			insp_quote:
				'“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
		},
		{
			id: 1,
			name: 'Felix Dusengimana',
			socials: [
				{
					name: 'twitter',
					link: 'https://twitter.com/felix_dusenge'
				},
				{
					name: 'linkedin',
					link: 'https://www.linkedin.com/in/felixdusengimana/'
				}
			],
			role: 'Co-Founder & CTO',
			avatar: felix,
			insp_quote:
				'“I am not a product of my circumstances. I am a product of my decisions.” - Stephen Covey'
		}
	];
</script>

<svelte:head>
	<title>Welcome to wildcards thinktank</title>
	<meta name="description" content="wildcards showcase what they do best" />
</svelte:head>

<section class="bg-[url('$lib/images/home.jpg')] py-10 bg-cover bg-no-repeat w-full min-h-[1000px]">
	<div class="mt-20">
		<picture>
			<source srcset={welcome} type="image/webp" />
			<img src={welcome_fallback} alt="Welcome" />
		</picture>
	</div>
	<p class="font-bold text-4xl max-w-[500px] mx-auto text-center">
		Join the Education Revolution with Wildcards
	</p>
	<p class="max-w-[500px] text-base mx-auto text-center mt-10 font-semibold">
		"Because of our passion for education, our mission is to reduce high rate of school dropouts in
		Rwanda by providing modernized equipments and other facilities to further their learning."
	</p>
</section>

<section id="solution" class="mt-20 flex gap-4 w-fit mx-auto">
	<div class="max-w-[500px]">
		<h1 class="text-center">Problem Statement</h1>
		<p class="text-center">
			According to UNICEF, in academic year of 2020/21 a lot of school-aged children dropped out
			with 11.3 percent of boys and 7.7 percent of girls . How will provision of modernized
			equipments(computers and books) reduce education exclusion to less than 5% by 2027?
		</p>
	</div>
	<div class="max-w-[500px]">
		<h1 class="text-center">Our Solution</h1>
		<p class="text-center">
			Our solution is a program called <b>empowerME</b> which will provide modernized equipments to schools
			in need. We will also provide books to students who can't afford them. And also we will create
			a vacation trainings for dropouts to learn more about technology and how to use it to solve problems
			in their communities.
		</p>
	</div>
</section>

<section id="about" class="mt-40">
	<div class="max-w-[500px] mx-auto">
		<h1 class="text-center">About Us</h1>
		<p class="text-center">
			We are a team of passionate individuals who believe that education is the key to a better
			future. We are committed to providing the best education to everyone, regardless of their
			background and ability.
		</p>
	</div>
</section>

<section id="team" class="mt-5">
	<div class="max-w-[500px] mx-auto">
		<h1 class="text-center">Our Team</h1>
	</div>
	<div class="grid grid-cols-3 gap-4 max-w-[1200px] mx-auto mt-4">
		{#each team as item, index (item.id)}
			<div class="flex flex-col h-full">
				<img alt="{item.name}  profile" class="h-full" src={item.avatar} />
				<div class="bg-white border shadow p-4">
					<p class="text-center font-bold">{item.name}</p>
					<p class="text-center">{item.role}</p>
					<div class="flex justify-center gap-2">
						{#each item.socials as social}
							<a href={social.link} target="_blank" rel="noopener noreferrer">
								{#if social.name === 'twitter'}
									<svg
										width="18"
										height="18"
										viewBox="0 0 48 48"
										fill="none"
										xmlns="http://www.w3.org/2000/svg"
									>
										<path
											d="M36.6526 3.80782H43.3995L28.6594 20.6548L46 43.5798H32.4225L21.7881 29.6759L9.61989 43.5798H2.86886L18.6349 25.56L2 3.80782H15.9222L25.5348 16.5165L36.6526 3.80782ZM34.2846 39.5414H38.0232L13.8908 7.63408H9.87892L34.2846 39.5414Z"
											fill="black"
										/>
									</svg>
								{/if}
								{#if social.name === 'linkedin'}
									<svg
										width="18"
										height="18"
										viewBox="0 0 48 48"
										fill="none"
										xmlns="http://www.w3.org/2000/svg"
									>
										<g clip-path="url(#clip0_17_32)">
											<path
												d="M44.4567 0H3.54333C2.60358 0 1.70232 0.373315 1.03782 1.03782C0.373315 1.70232 0 2.60358 0 3.54333V44.4567C0 45.3964 0.373315 46.2977 1.03782 46.9622C1.70232 47.6267 2.60358 48 3.54333 48H44.4567C45.3964 48 46.2977 47.6267 46.9622 46.9622C47.6267 46.2977 48 45.3964 48 44.4567V3.54333C48 2.60358 47.6267 1.70232 46.9622 1.03782C46.2977 0.373315 45.3964 0 44.4567 0ZM14.3067 40.89H7.09V17.9667H14.3067V40.89ZM10.6933 14.79C9.87473 14.7854 9.07583 14.5384 8.39747 14.0802C7.71911 13.622 7.19168 12.9731 6.88175 12.2154C6.57183 11.4577 6.4933 10.6252 6.65606 9.82291C6.81883 9.02063 7.2156 8.28455 7.79631 7.70756C8.37702 7.13057 9.11563 6.73853 9.91893 6.58092C10.7222 6.42331 11.5542 6.50719 12.3099 6.82197C13.0656 7.13675 13.7111 7.66833 14.1649 8.34962C14.6188 9.03092 14.8606 9.83138 14.86 10.65C14.8677 11.1981 14.765 11.7421 14.558 12.2496C14.351 12.7571 14.044 13.2178 13.6551 13.6041C13.2663 13.9905 12.8037 14.2946 12.2948 14.4983C11.786 14.702 11.2413 14.8012 10.6933 14.79ZM40.9067 40.91H33.6933V28.3867C33.6933 24.6933 32.1233 23.5533 30.0967 23.5533C27.9567 23.5533 25.8567 25.1667 25.8567 28.48V40.91H18.64V17.9833H25.58V21.16H25.6733C26.37 19.75 28.81 17.34 32.5333 17.34C36.56 17.34 40.91 19.73 40.91 26.73L40.9067 40.91Z"
												fill="#0A66C2"
											/>
										</g>
										<defs>
											<clipPath id="clip0_17_32">
												<rect width="48" height="48" fill="white" />
											</clipPath>
										</defs>
									</svg>
								{/if}
								{#if social.name === 'facebook'}
									<svg
										width="18"
										height="18"
										viewBox="0 0 48 48"
										fill="none"
										xmlns="http://www.w3.org/2000/svg"
									>
										<g clip-path="url(#clip0_17_24)">
											<path
												d="M48 24C48 10.7453 37.2547 0 24 0C10.7453 0 0 10.7453 0 24C0 35.255 7.74912 44.6995 18.2026 47.2934V31.3344H13.2538V24H18.2026V20.8397C18.2026 12.671 21.8995 8.8848 29.9194 8.8848C31.44 8.8848 34.0637 9.18336 35.137 9.48096V16.129C34.5706 16.0694 33.5866 16.0397 32.3645 16.0397C28.4294 16.0397 26.9088 17.5306 26.9088 21.4061V24H34.7482L33.4013 31.3344H26.9088V47.8243C38.7926 46.3891 48.001 36.2707 48.001 24H48Z"
												fill="#0866FF"
											/>
											<path
												d="M33.4003 31.3344L34.7472 24H26.9078V21.4061C26.9078 17.5306 28.4285 16.0397 32.3635 16.0397C33.5856 16.0397 34.5696 16.0694 35.136 16.129V9.48096C34.0627 9.1824 31.439 8.8848 29.9184 8.8848C21.8986 8.8848 18.2016 12.671 18.2016 20.8397V24H13.2528V31.3344H18.2016V47.2934C20.0582 47.7542 22.0003 48 23.999 48C24.983 48 25.9536 47.9395 26.9069 47.8243V31.3344H33.3994H33.4003Z"
												fill="white"
											/>
										</g>
										<defs>
											<clipPath id="clip0_17_24">
												<rect width="48" height="48" fill="white" />
											</clipPath>
										</defs>
									</svg>
								{/if}
								{#if social.name === 'instagram'}
									<svg
										width="18"
										height="18"
										viewBox="0 0 48 48"
										fill="none"
										xmlns="http://www.w3.org/2000/svg"
									>
										<g clip-path="url(#clip0_17_27)">
											<path
												d="M24 4.32187C30.4125 4.32187 31.1719 4.35 33.6938 4.4625C36.0375 4.56562 37.3031 4.95938 38.1469 5.2875C39.2625 5.71875 40.0688 6.24375 40.9031 7.07812C41.7469 7.92188 42.2625 8.71875 42.6938 9.83438C43.0219 10.6781 43.4156 11.9531 43.5188 14.2875C43.6313 16.8187 43.6594 17.5781 43.6594 23.9813C43.6594 30.3938 43.6313 31.1531 43.5188 33.675C43.4156 36.0188 43.0219 37.2844 42.6938 38.1281C42.2625 39.2438 41.7375 40.05 40.9031 40.8844C40.0594 41.7281 39.2625 42.2438 38.1469 42.675C37.3031 43.0031 36.0281 43.3969 33.6938 43.5C31.1625 43.6125 30.4031 43.6406 24 43.6406C17.5875 43.6406 16.8281 43.6125 14.3063 43.5C11.9625 43.3969 10.6969 43.0031 9.85313 42.675C8.7375 42.2438 7.93125 41.7188 7.09688 40.8844C6.25313 40.0406 5.7375 39.2438 5.30625 38.1281C4.97813 37.2844 4.58438 36.0094 4.48125 33.675C4.36875 31.1438 4.34063 30.3844 4.34063 23.9813C4.34063 17.5688 4.36875 16.8094 4.48125 14.2875C4.58438 11.9437 4.97813 10.6781 5.30625 9.83438C5.7375 8.71875 6.2625 7.9125 7.09688 7.07812C7.94063 6.23438 8.7375 5.71875 9.85313 5.2875C10.6969 4.95938 11.9719 4.56562 14.3063 4.4625C16.8281 4.35 17.5875 4.32187 24 4.32187ZM24 0C17.4844 0 16.6688 0.028125 14.1094 0.140625C11.5594 0.253125 9.80625 0.665625 8.2875 1.25625C6.70312 1.875 5.3625 2.69062 4.03125 4.03125C2.69063 5.3625 1.875 6.70313 1.25625 8.27813C0.665625 9.80625 0.253125 11.55 0.140625 14.1C0.028125 16.6687 0 17.4844 0 24C0 30.5156 0.028125 31.3312 0.140625 33.8906C0.253125 36.4406 0.665625 38.1938 1.25625 39.7125C1.875 41.2969 2.69063 42.6375 4.03125 43.9688C5.3625 45.3 6.70313 46.125 8.27813 46.7344C9.80625 47.325 11.55 47.7375 14.1 47.85C16.6594 47.9625 17.475 47.9906 23.9906 47.9906C30.5063 47.9906 31.3219 47.9625 33.8813 47.85C36.4313 47.7375 38.1844 47.325 39.7031 46.7344C41.2781 46.125 42.6188 45.3 43.95 43.9688C45.2812 42.6375 46.1063 41.2969 46.7156 39.7219C47.3063 38.1938 47.7188 36.45 47.8313 33.9C47.9438 31.3406 47.9719 30.525 47.9719 24.0094C47.9719 17.4938 47.9438 16.6781 47.8313 14.1188C47.7188 11.5688 47.3063 9.81563 46.7156 8.29688C46.125 6.70312 45.3094 5.3625 43.9688 4.03125C42.6375 2.7 41.2969 1.875 39.7219 1.26562C38.1938 0.675 36.45 0.2625 33.9 0.15C31.3313 0.028125 30.5156 0 24 0Z"
												fill="#000100"
											/>
											<path
												d="M24 11.6719C17.1938 11.6719 11.6719 17.1938 11.6719 24C11.6719 30.8062 17.1938 36.3281 24 36.3281C30.8062 36.3281 36.3281 30.8062 36.3281 24C36.3281 17.1938 30.8062 11.6719 24 11.6719ZM24 31.9969C19.5844 31.9969 16.0031 28.4156 16.0031 24C16.0031 19.5844 19.5844 16.0031 24 16.0031C28.4156 16.0031 31.9969 19.5844 31.9969 24C31.9969 28.4156 28.4156 31.9969 24 31.9969Z"
												fill="#000100"
											/>
											<path
												d="M39.6937 11.1844C39.6937 12.7782 38.4 14.0625 36.8156 14.0625C35.2219 14.0625 33.9375 12.7688 33.9375 11.1844C33.9375 9.59065 35.2313 8.30627 36.8156 8.30627C38.4 8.30627 39.6937 9.60003 39.6937 11.1844Z"
												fill="#000100"
											/>
										</g>
										<defs>
											<clipPath id="clip0_17_27">
												<rect width="48" height="48" fill="white" />
											</clipPath>
										</defs>
									</svg>
								{/if}
							</a>
						{/each}
					</div>

					<article class="mt-4">
						<p class="text-center">{item.insp_quote}</p>
					</article>
				</div>
			</div>
		{/each}
	</div>
</section>
<section id="challenges">
	<ELabChallenges />
</section>

<style>
	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}
</style>
