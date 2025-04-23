<script>
	import Hero from "$components/Hero.svelte";
	import Main from "$components/Main.svelte";
	import Footer from "$components/Footer.svelte";
	import copy from "$data/copy.json";
	import Landing from "./Landing.svelte";
</script>

<!-- <Hero />
<Main />
<Footer /> -->
<Landing />

<h1>{copy.byline}</h1>
<p>Text testing 123 if i start messing around is this gonna properly show?</p>

<p class="story-section">{copy.familytogether}</p>
<p>{copy.familyseparation}</p>

<style>
	.family-together {
		color: blue;
		font-weight: bold;
	}
</style>
