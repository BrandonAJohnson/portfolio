<script>
	import Step from "./Step.svelte";


	const steps = [
		{
			name: 'EDPlan',
			href: 'https://www.edplan.com/',
			icon: 'fa-solid fa-school',
			content: 'Senior Software Engineer and Tech Lead for a Special Education Management Platform',
		},
		{
			name: 'TMDB Movie Browser',
			href: 'https://github.com/BrandonAJohnson/MovieBrowser',
			icon: 'fa-solid fa-film',
			content: 'React Web App that consumes the TMDB API',
		},
		{
			name: 'This Portfolio',
			href: 'https://github.com/BrandonAJohnson/portfolio',
			icon: 'fa-solid fa-film',
			content: 'We love Svelte around here',
		},
		{
			name: 'Steering Behaviors',
			href: '', // insert github url
			icon: 'fa-solid fa-arrow-trend-up',
			content: 'Web based implementation of AI Steering Behaviors',
		},
		{
			name: 'Deep Learning Pacman',
			href: '', // insert github url
			icon: 'fa-solid fa-ghost',
			content: 'Web based implementation of AI Steering Behaviors',
		},
		{
			name: 'Web Dataset Analyzer',
			href: 'https://github.com/BrandonAJohnson/SENG650',
			icon: 'fa-solid fa-chart-bar',
			content: 'School Project for producing graphs for datasets',

		},
		{
			name: 'Halo',
			href: 'https://m.twitch.tv/clip/CoyHonestTildeMau5-hc45_84aMe7r9yZ-',
			icon: 'fa-solid fa-gamepad',
			content: 'HRL Champs Division Semi-Finals'
		},
		{
			name: 'Reading',
			href: 'https://www.goodreads.com/user/show/161803074-brandon-johnson',
			icon: 'fa-solid fa-book',
			content: 'I enjoy reading :)',
		},
	];

	const favTech = [
		{
			name: 'HTML',
			image: '/images/html5.png',
		},
		{
			name: 'CSS',
			image: '/images/css.png',
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
			image: '/images/svelte.png',
		},
		{
			name: 'TailwindCSS',
			image: '/images/tailwind.png',
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
				Hello! I'm <span class="text-yellow-400">Brandon Johnson</span><br>
				and I'm a Full Stack Web <span class="text-yellow-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-yellow-400">preferred tech</span> includes
				{#each favTech as tech, i}
					{' '}{tech.name}
					{#if tech.image}
						<img src={tech.image} alt={tech.name} class="h-8 inline-block"/>
					{/if}
				{/each}
			</p>
			<a href="#" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
				<div class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-50 group-hover:translate-x-full z-0 duration-200"></div>
				<h4 class="relative z-9">Contact Me &rarr;</h4>
			</a>
		</div>
		<div class="relative shadow-2xl grid place-items-center">
			<!-- need another picture -->
			<img src="/images/me-transparent.png" alt="profile" class="object-cover z-[2] max-h-[50vh]"/>
		</div>
	</section>
	<section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col text-center">
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Some projects/activities I have worked on</h3>
		</div>
		<div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
			{#each steps as step}
				<Step step={step}>
					{step.content || ''}
				</Step>
			{/each}
		</div>
		<div class="flex flex-col text-center">
			<h3 class="font-semibold text-xl sm:text-2xl md:text-3xl">A little more...</h3>
		</div>
		<a href="https://github.com/BrandonAJohnson" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:bg-white hover:text-blue-900 duration-200">
			Check out my github! <i class="fa-solid fa-code"></i>
		</a>
	</section>
	<section id="blog" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col text-center">
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Some random thoughts</h3>
		</div>
	</section>
	<section id="links" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col text-center">
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Where you can find me</h3>
		</div>
	</section>
</main>