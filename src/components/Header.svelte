<script>
 	export let y;

	let tabs = [
		{
			name: 'Home',
			link: '#home'
		},
		{
			name: 'Projects',
			link: '#projects'
		},
		{
			name: 'About Me',
			link: '#aboutme'
		},
		{
			name: 'Blog',
			link: '#blog'
		},
		{
			name: 'Links',
			link: '#links'
		},
	]
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid ' + ((y > 0) ? ' py-4 bg-slate-950 border-slate-950 ' : ' py-6 bg-transparent border-transparent ')}>
	<h1 class="text-4xl"><img src='/images/me-transparent.png' alt='Brandon Johnson' class="h-20 w-20 inline-block"/> <b class="font-extrabold">Brandon</b> Johnson</h1>
	<div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
		{#each tabs as tab, i}
			<a class="duration-200 hover:text-amber-400" href={tab.link}>
				<p>{tab.name}</p>
			</a>
		{/each}
	</div>
	<a href="#" target="_blank" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-blue-900 text-white">
		<div class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-50 group-hover:translate-x-full z-0 duration-200"></div>
		<h4 class="relative z-9">Contact Me</h4>
	</a>
</header>