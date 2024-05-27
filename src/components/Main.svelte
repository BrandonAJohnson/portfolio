<script>
	const favTech = [
		{
			name: 'HTML',
			image: '/images/html5.png',
		},
		{
			name: 'CSS',
			image: '/images/css.jpg',
		},
		{
			name: 'JavaScript',
			image: '/images/javascript.png',
		},
		{
			name: 'TypeScript',
			image: '/images/typescript.png',
		},
		{
			name: 'Svelte',
			image: '/images/svelte.jpg',
		},
		{
			name: 'TailwindCSS',
			image: '/images/tailwind.jpg',
		},
		{
			name: 'Node.js',
			image: '/images/nodejs.png',
		},
		{
			name: 'SQL',
			image: '/images/sql.png',
		},
		{
			name: 'Python',
			image: '/images/python.png',
		},
	];
</script>

<main class="flex flex-col flex-1">
	<section id="aboutme" class="grid grid-cols-1 lg:grid-cols-1 gap-10 py-8 sm:py-14">
		<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
			<h2 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				Hello! I'm <span class="text-yellow-400">Brandon</span> Johnson<br>
				Full Stack <span class="text-yellow-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-yellow-400">preferred tech</span> includes
				{#each favTech as tech, i}
					{' '}{tech.name}
					{#if tech.image}<img src={tech.image} alt={tech.name} class="h-8 inline-block"/>{/if}
				{/each}
			</p>
		</div>
	</section>
</main>