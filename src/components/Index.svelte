<script>
	import Hero from "$components/Hero.svelte";
	import Main from "$components/Main.svelte";
	import Footer from "$components/Footer.svelte";
	import Decision from "$components/Decision.svelte";

	let choices = ["Option 1", "Option 2", "Option 3"];
	let outcomes = [
		"This is the outcome of option 1. It should be a long paragraph that describes what happens when the user chooses this option. It can be as long as you want, but it should be at least a few sentences long.",
		"This is the outcome of option 2. It should be a long paragraph that describes what happens when the user chooses this option. It can be as long as you want, but it should be at least a few sentences long.",
		"This is the outcome of option 3. It should be a long paragraph that describes what happens when the user chooses this option. It can be as long as you want, but it should be at least a few sentences long."
	];
</script>

<Decision decisionText="Choose one of these options." {choices} {outcomes} />
