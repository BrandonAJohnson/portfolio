<script>
	import '../app.css';
    import Footer from '../components/Footer.svelte';
    import Header from '../components/Header.svelte';

	 let y = 0;
	 let innerHeight = 0;
	 let innerWidth = 0;

	function goToTop() {
		document.body.scrollIntoView();
	}
</script>

<div class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen">
	<div class={"fixed bottom-0 width-full duration-200 flex p-10 z-[10] " + (y > 0 ? ' opacity-full pointer-events-auto ' : ' pointer-events-none opacity-0 ')}>
		<button class="rounded-full aspect-square ml-auto bg-slate-900 text-amber-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer" on:click={goToTop}>
			<i class="fa-solid fa-arrow-up grid place-items-center aspect-square"/>
		</button>
	</div>
	<Header y/>
	<slot/>
	<Footer/>
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth/>

