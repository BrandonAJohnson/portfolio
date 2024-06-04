<script>
// @ts-nocheck

	import Step from "./Step.svelte";
	import Chart from "./Chart.svelte";

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

	const skills = [
		{
			name: 'A First Generation College Graduate',
			image: '/images/wvu.png',
			description: "I am the only member of my family to ever graduate from college, and I have done it twice! I received a Master's Degree in Software Engineering in 2023 from West Virginia University. Prior to that I attended Bluefield State University and received a Bachelor's in Computer Science."
		},
		{
			name: 'A Husband and Father',
			description: "I have been married to my wife Manda since 2012. We have 3 children: Emma, Jacob and Elaina. When I am not coding, I am normally spending time with my family.",
		},
		{
			name: 'A Lifelong Learner',
			description: 'I am constantly taking courses, reading tech-related books, and coding. In this field, if you aren\'t pushing forward, you will fall behind. I never want to settle and think I am "good enough".'
		},
	];


	let type = 'bar';
	let data = {
		labels: ['HTML', 'CSS', 'JavaScript', 'SQL', 'Perl', 'TypeScript', 'AngularJS', 'C#', 'Svelte', 'React',],
		datasets: [
			{
				axis: 'y',
				label: 'Years',
				data: [
					10, // html
					10, // css
					10, // js
					8, // sql
					8, // perl
					5, // ts
					5, // angularjs
					3, // c#
					2, // svelte
					1 // react
				],
				fill: false,
				backgroundColor: [
					'rgba(255, 99, 132, 0.3)',
					'rgba(255, 159, 64, 0.3)',
					'rgba(255, 205, 86, 0.3)',
					'rgba(75, 192, 192, 0.3)',
					'rgba(54, 162, 235, 0.3)',
					'rgba(153, 102, 255, 0.3)',
					'rgba(201, 203, 207, 0.3)'
				],
				borderColor: [
					'rgb(255, 99, 132)',
					'rgb(255, 159, 64)',
					'rgb(255, 205, 86)',
					'rgb(75, 192, 192)',
					'rgb(54, 162, 235)',
					'rgb(153, 102, 255)',
					'rgb(201, 203, 207)'
				],
				borderWidth: 3
			}
		]
	};

	let options = {
		plugins: {
			legend: {
				display: false
			}
		},
		indexAxis: 'y',
		elements: {
			bar: {
				borderWidth: 3,
			},
		},
		responsive: true,
	};
</script>

<main class="flex flex-col flex-1">
	<section id="home" class="grid grid-cols-1 lg:grid-cols-1 gap-10 py-8 sm:py-14">
		<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
			<h2 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				Hello! I'm <span class="text-yellow-400">Brandon Johnson</span><br>
				and I'm a <span class="text-yellow-400">Full Stack Web Developer</span>
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
			<a href="mailto:brandonajohnson09@gmail.com" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
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
			<h3 class="font-semibold text-xl sm:text-2xl md:text-3xl">Other things I have worked on...</h3>
		</div>
		<a href="https://github.com/BrandonAJohnson" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:bg-white hover:text-blue-900 duration-200">
			Check out my github! <i class="fa-solid fa-code"></i>
		</a>
	</section>
	<section id="aboutme" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
		<div class="flex flex-col gap-2 relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700
			after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 py-6">
			<h6 class="text-lg sm:text-xl md:text-2xl mx-auto">Want to know more?</h6>
			<p class="mx-auto font-semibold text-lg sm:text-xl md:text-2xl mb-8 text-amber-400">I am...</p>
			<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
				{#each skills as skill, index}
					<div class="flex gap-6 sm:gap-8">
						<p class="text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semi-bold">{index<9?0:''}{index+1}</p>
						<div class="flex flex-col gap-6 sm:gap-8">
							<h3 class="text-2xl sm:text-3xl md:5xl">
								{#if skill.image}
									<img src={skill.image} alt={skill.name} class="inline-block h-10 w-auto"/>
								{/if}
								{skill.name}
							</h3>
							<p>{skill.description}</p>
						</div>
					</div>
				{/each}
			</div>
			<h5 class="text-2xl sm:text-3xl font-semibold text-center mt-10">My <span class="text-bold text-amber-400">Experience</span> and <span class="text-bold text-blue-400">Skill Set</span></h5>
			<div class="mb-8 flex flex-col gap-2">
				<Chart options={options} type={type} data={data}></Chart>
			</div>
			<div class="flex flex-col overflow-x-scroll gap-10 max-x-[800px] mx-auto w-full">
				<table class="bg-white text-slate-700 rounded text-center">
					<thead class="border-b border-solid border-slate-200">
						<tr>
							<th></th>
							<th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
							<th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
							<th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
							<th class="whitespace-nowrap p-2 px-4 bg-blue-700 text-white">Me</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b border-solid border-slate-200">
							<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-bold text-sm whitespace-nowrap">Programming</td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-green-500 text-2xl"></i></td>
						</tr>
						<tr class="border-b border-solid border-slate-200">
							<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-bold text-sm whitespace-nowrap">Leadership</td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-green-500 text-2xl"></i></td>
						</tr>
						<tr class="border-b border-solid border-slate-200">
							<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-bold text-sm whitespace-nowrap">Critical Thinking</td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-green-500 text-2xl"></i></td>
						</tr>
						<tr class="border-b border-solid border-slate-200">
							<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-bold text-sm whitespace-nowrap">Analysis & Design</td>
							<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
							<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-green-500 text-2xl"></i></td>
						</tr>
						<tr class="border-b border-solid border-slate-200">
							<td class="border-r border-solid border-white pl-4 pr-8 py-4 font-bold text-sm whitespace-nowrap">Training & Mentoring</td>
							<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-slate-500"></i></td>
							<td><i class="fa-solid fa-check text-green-500 text-2xl"></i></td>
						</tr>
					</tbody>
				</table>
			</div>
			<div class="mx-auto -mt-12 italic sm:hidden opacity-50">
				<p>Scroll to see more &rarr;</p>
			</div>
		</div>
	</section>
	<section id="blog" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col text-center">
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Some random thoughts</h3>
		</div>
	</section>
	<section id="links" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col text-center">
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Where you can find me</h3>
			<h3 class="m-8"><a href="https://www.linkedin.com/in/brandon-johnson-662256203/" target="_blank" class="inline-block"><img class="h-16 w-auto" src="/images/linkedin.png" alt="linkedin"/></a></h3>
		</div>
	</section>
</main>