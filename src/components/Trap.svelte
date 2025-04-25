<p>hopefully coded for line opening and making a trap door</p>

<div class="line"><hr /></div>

<!-- <script>
	import { onMount } from "svelte";
	let open = false;
	let trapRef;

	onMount(() => {
		console.log("trapRef:", trapRef);
		const observer = new IntersectionObserver(
			([entry]) => {
				console.log("Intersection entry:", entry); // Log the entry object
				if (entry.isIntersecting && !open) {
					open = true;
					console.log("Intersection observed, open set to true");
				}
			},
			{ threshold: 0.5 }
		);

		if (trapRef) {
			observer.observe(trapRef);
			console.log("Observer set up");
		}

		// Reset animation if user scrolls to the very top of the page
		window.addEventListener("scroll", () => {
			if (window.scrollY === 0) {
				open = false;
				console.log("Scroll reset, open set to false");
			}
		});
	});
	$effect(() => {
		console.log("open is now:", open); // Log the value of open whenever it changes
	});
</script>

<div bind:this={trapRef} class="trap-floor {open ? 'open' : ''}">
	{#each Array(5) as _, i}
		<div class="trap-line">
			<div class="moving-line left" style="transition-delay: {i * 50}ms;"></div>
			<div
				class="moving-line right"
				style="transition-delay: {i * 50}ms;"
			></div>
		</div>
	{/each}
</div>

<style>
	.trap-floor {
		position: relative;
		height: 100px;
		width: 100%;
		background: #f0f0f0;
		overflow: hidden;
		margin-top: 100vh; /* Just for demo scroll spacing */
	}

	.trap-line {
		position: absolute;
		left: 0;
		width: 100%;
		height: 3px;
		top: 0;
	}

	.trap-line:nth-child(2) {
		top: 20px;
	}
	.trap-line:nth-child(3) {
		top: 40px;
	}
	.trap-line:nth-child(4) {
		top: 60px;
	}
	.trap-line:nth-child(5) {
		top: 80px;
	}

	.moving-line {
		position: absolute;
		height: 3px;
		background: #1446ff;
		width: 50%;
		transition: transform 0.3s ease;
		transform: translate3d(0, 0, 0);
	}

	.moving-line.right {
		left: 50%;
	}

	.open .moving-line.left {
		transform: translate3d(-80px, 0, 0);
	}
	.open .moving-line.right {
		transform: translate3d(80px, 0, 0);
	}
</style> -->

<style>
	.line {
		width: 100%;
		height: 50px;
		background-color: transparent;
		margin: 20px 0;
		color: white;
	}
	.line hr {
		border: none;
		height: 5px;
		background-color: white;
	}
</style>
