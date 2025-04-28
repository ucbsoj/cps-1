<script>
	import Footer from "$components/Footer.svelte";
	import Decision from "$components/Decision.svelte";
	import copy from "$data/copy.json";
	import Landing from "./Landing.svelte";
	import Meta from "$components/Meta.svelte";
	import Trap from "$components/Trap.svelte";
	import DemoScrolly from "$components/demo/Demo.Scrolly.svelte";
	import Phone from "./Phone.svelte";
	import DemoImages from "$components/demo/Demo.Images.svelte";
	import Demo from "./demo/Demo.Hero.svelte";
	import Intro from "./Intro.svelte";
</script>

<div class="content">
	<Landing />
	<Intro />
	<!-- <div class="writing">
		<p class="family-together">{copy.familytogether}</p> -->
	<!-- <p class="textcaption">{copy.textcaption}</p> -->
	<!-- <p class="familytogethercallsign">{copy.familytogethercallsign}</p> -->
	<!-- <p class="familyseparation">{copy.familyseparation}</p>
		<p class="child">{copy.child}</p>
		<p class="childwelfareagencies">{copy.childwelfareagencies}</p> -->
	<!-- </div> -->
	<Phone />
	<!-- <Trap /> -->
	<article>
		{#each copy.tree as { type, value, decisionText, choices, outcomes }}
			{#if type === "text"}
				<p>{@html value}</p>
			{:else if type === "decision"}
				<Decision {decisionText} {choices} {outcomes} />
			{/if}
		{/each}
	</article>
</div>

<style>
	article {
		max-width: 700px;
		margin: 0 auto;
		background-color: #4a5668;
	}

	.family-together {
		font-weight: bold;
	}
	.content {
		background-color: #4a5668;
		color: #fff;
		font-family: "Sansita", sans-serif;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.writing {
		margin-left: 10%;
		margin-right: 10%;
		align-items: center;
		justify-content: center;
		display: flex;
		flex-direction: column;
	}
</style>
