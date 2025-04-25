<script>
	import Hero from "$components/Hero.svelte";
	import Main from "$components/Main.svelte";
	import Footer from "$components/Footer.svelte";
	import Decision from "$components/Decision.svelte";
	import copy from "$data/copy.json";

	/*
	const copy = [
		{
			type: "text",
			value: "This is my intro paragraph. This starts out the story."
		},
		{
			type: "decision",
			decisionText: "Make this first decision.",
			choices: ["Option 1", "Option 2", "Option 3"],
			outcomes: [
				[
					{
						type: "text",
						value: "This is the outcome of choice 1. It ends in a dead end."
					},
					{ type: "text", value: "Oh well!" }
				],
				[
					{
						type: "text",
						value:
							"This one has a paragraph followed by another decision to make."
					},
					{
						type: "decision",
						decisionText: "Make this second decision.",
						choices: ["Option 1", "Option 2"],
						outcomes: [
							[
								{
									type: "text",
									value:
										"This is the outcome of choice 1. It ends in a dead end."
								},
								{ type: "text", value: "Oh well!" }
							],
							[
								{
									type: "text",
									value:
										"This is the outcome of choice 2. It ends in a dead end."
								},
								{ type: "text", value: "Oh well!" }
							]
						]
					}
				],
				[
					{
						type: "text",
						value: "This is the outcome of choice 3. It ends in a dead end."
					},
					{ type: "text", value: "Womp womp." }
				]
			]
		}
	];
	*/
</script>

<article>
	{#each copy.tree as { type, value, decisionText, choices, outcomes }}
		{#if type === "text"}
			<p>{@html value}</p>
		{:else if type === "decision"}
			<Decision {decisionText} {choices} {outcomes} />
		{/if}
	{/each}
</article>

<style>
	article {
		max-width: 700px;
		margin: 0 auto;
	}
</style>
