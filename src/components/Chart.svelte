<script lang="ts">
	import { Chart, type ChartConfiguration, type ChartData, type ChartOptions, type ChartType } from "chart.js/auto";
	import { onMount } from "svelte";

	export let data: ChartData;
	export let type: ChartType;
	export let options: ChartOptions;

	onMount(() => {
		const ctx = <HTMLCanvasElement>document.getElementById('chart');
		new Chart(ctx,
			<ChartConfiguration>{
				data,
				type,
				options
			},
		);
	});
</script>

<div>
	<canvas id="chart"></canvas>
</div>