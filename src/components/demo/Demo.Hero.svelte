<script>
	import Hero from "$components/helpers/Hero.svelte";

	/* 
		The Hero component is a full-width image or video with a headline, dek, and byline (these are optional).
		- hed: The headline for the hero.
		- dek: The dek for the hero.
		- byline: The byline for the hero.
		- src: The source of the image or video file.
		- alt: The alt text, if it's an image.
	*/
</script>

<Hero
	hed="Minahil is awesome"
	dek="Welcome valued guests"
	byline="By This Person and That Person"
	src="/demo/assets/test.jpg"
	alt="A lake and some clouds"
/>

<!-- Hero with video -->
<!-- <Hero
	hed="This is a placeholder headline"
	dek="Welcome to this demo"
	byline="By This Person and That Person"
	src="demo/assets/test.mp4"
	alt="Flourescent jellyfish moving around"
/> -->
