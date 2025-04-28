<script>
	import Decision from "$components/Decision.svelte";

	let { decisionText = "", choices = [], outcomes = [] } = $props();

	const wheelWidth = "24rem";
	const textWidth = "28em";
	const dur = "500ms";

	let activeI = $state(undefined);
	let degrees = $state(choices.length === 3 ? [60, -60, 0] : [60, -60]);
	let r = $derived(activeI !== undefined ? degrees[activeI] : 0);

	const onClick = (i) => {
		activeI = i;
	};
</script>

<div
	class="decision"
	style={`--wheel-width: ${wheelWidth}; --text-width: ${textWidth}; --dur: ${dur}`}
>
	<p class="decision-text">{decisionText}</p>

	<div class="choices" style:transform={`rotate(${-r}deg)`}>
		{#each choices as choice, i}
			{@const rotate = degrees[i]}
			<div class="choice">
				<div class="rotate" style:transform={`rotate(${rotate}deg)`}>
					<button
						style="transform: rotate({-rotate + r}deg)"
						onclick={() => onClick(i)}>{choice}</button
					>
				</div>
			</div>
		{/each}
	</div>

	<div class="outcomes" style:transform={`rotate(${-r}deg)`}>
		{#each outcomes as outcome, i}
			{@const rotate = degrees[i]}
			<div
				class="outcome"
				class:active={activeI === i}
				style:transform={`rotate(${rotate}deg) translateY(4.5em)`}
			>
				{#each outcome.outcome as { type, value, decisionText, choices, outcomes, src, alt }}
					{#if type === "text"}
						<p>{@html value}</p>
					{:else if type === "decision"}
						<Decision {decisionText} {choices} {outcomes} />
					{:else if type === "img"}
						<img {src} {alt} />
					{/if}
				{/each}
			</div>
		{/each}
	</div>
</div>

<style>
	.decision {
		position: relative;
		margin: 5rem 0;
		background-color: #4a5668;
	}

	/* choices, the circle */

	.choices {
		position: relative;
		height: var(--wheel-width);
		width: var(--wheel-width);
		background: var(--color-gray-100);
		border-radius: 50%;
		margin: 0 auto;
		transform-origin: 50% 50%;
		transition: transform var(--dur) ease-out;
	}

	.rotate {
		transition: transform var(--dur) ease-out;
	}

	.choice {
		position: absolute;
	}

	.choice:nth-of-type(1) {
		top: 50%;
		left: 0;
		transform: translate(-50%, -50%);
	}

	.choice:nth-of-type(2) {
		right: 0;
		top: 50%;
		transform: translate(50%, -50%);
	}

	.choice:nth-of-type(3) {
		left: 50%;
		top: 100%;
		transform: translate(-50%, -50%);
	}

	.decision-text {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		text-align: center;
		z-index: 10;
		color: black;
	}

	button {
		transition: transform var(--dur) ease-out;
	}

	/* outcomes */

	.outcomes {
		position: relative;
		transition: transform var(--dur) ease-out;
		transform-origin: 50% calc(var(--wheel-width) / -2);
		width: var(--text-width);
		margin: 0 auto;
		z-index: 0;
		background-color: #4a5668;
	}

	.outcome {
		position: absolute;
		transform-origin: 50% calc(var(--wheel-width) / -2);
		top: 0;
		left: 0;
		width: 100%;
		max-width: var(--text-width);
		transition: opacity var(--dur) ease-out;
		opacity: 0.2;
		filter: blur(4px);
		background-color: #4a5668;
	}

	.active {
		opacity: 1;
		filter: blur(0);
		background-color: #4a5668;
	}
</style>
