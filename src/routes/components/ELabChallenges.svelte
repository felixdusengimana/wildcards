<script>
	const tabs = [
		'All',
		'Challenge 1',
		'Challenge 2',
		'Challenge 3',
		'Challenge 4',
		'Challenge 5',
		'Challenge 6'
	];
	let activeIndex = 0;

	$: challenges = [
		{
			id: 1,
			title: 'Introduction',
			description: 'This is where the journey begins',
			content: `
                <h1>Meet the team</h1>
                <iframe class="responsiveIframe" src="https://www.youtube.com/embed/R2KuL87u5xI?si=zGUw8BDRj9ZVE3BU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
                `
		},
		{
			id: 2,
			title: 'Discover Africa',
			description: 'Creating story about an african character',
			content: `
            <h1>Read the story</h1>
            <iframe class="responsiveIframe" src="https://docs.google.com/presentation/d/e/2PACX-1vRtvJvVve2Lg9TywS27x3oePKTDn2cKwOn6VorPfu-uGspscevtShM83YlU4rSqwBrxkqRjctQ6kCXY/embed?start=true&loop=false&delayms=60000" frameborder="0"  allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe> `
		},
		{
			id: 3,
			title: 'HELP-LAB',
			description: 'Helping people in need',
			content: `
            <h1>Watch the video</h1>
            <iframe class="responsiveIframe" src="https://www.youtube.com/embed/lJyd5J5XEdc?si=SHVBTR-PfZmQ-RO7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
            
            `
		},
		{
			id: 4,
			title: 'Hunt for Treasure',
			description: 'Interviewing MTN/Airtel agents',
			content: `
            <h1> Read findings</h1>
            <iframe class="responsiveIframe" src="https://docs.google.com/presentation/d/e/2PACX-1vROTkpLXpOHX3I3YWtl-168WRlvqLwjgeeU5n488CcoEJrQJylsBdvejbLYaePj7CI7kNZZONVv5GQT/embed?start=false&loop=false&delayms=60000" frameborder="0" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
            `
		},
		{
			id: 5,
			title: 'Launch Your Mission V2',
			description: 'Working on our mission',
			content: `
            <h1>Read our mission</h1>
            <iframe class="responsiveIframe" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRBib1XYEUfYF8lmBeOuskqIffEhC5uo-S9q3mm_9ZioknWydjrEUSmkdj5n6UMJbCM7THl0pwyLaly/pubhtml?widget=true&amp;headers=false"></iframe>
            `
		},
		{
			id: 6,
			title: 'Your Digital Print',
			description: 'Creating our website',
			content: `
            <h1>This is our website</h1>
            
            `
		}
	];

	// update iframe width when index!==0 to be 100% and height to be auto
</script>

<h1 class="text-center my-6">ELab Challenges Completed</h1>
<div class="max-w-[1200px] w-fit mx-auto">
	<div class="flex gap-2 flex-wrap mx-auto w-fit">
		{#each tabs as tab, index}
			<button
				class="px-3 py-2 rounded-md font-medium
            {activeIndex === index ? 'bg-blue-500 text-white' : 'bg-gray-100 text-gray-700'}"
				on:click={() => (activeIndex = index)}>{tab}</button
			>
		{/each}
	</div>

	<div class={activeIndex === 0 ? 'flex gap-4 w-full flex-wrap mt-4 justify-center' : 'w-full'}>
		{#each challenges as challenge}
			{#if activeIndex === 0 || activeIndex === challenge.id}
				<div class="bg-white rounded-md border {activeIndex == 0 ? 'w-[320px]' : 'w-[870px]'} p-2">
					<h3 class="text-lg font-medium">{challenge.title}</h3>
					<p class="text-gray-500">{challenge.description}</p>
					<div class="moreContent">{@html challenge.content}</div>
				</div>
			{/if}
		{/each}
	</div>
</div>

<style>
	.responsiveIframe {
		width: 910px;
	}
</style>
