<script>
	import copy from "$data/copy.json";
</script>

<div class="landing">
	<div class="image-container">
		<img src="/images/new.png" alt="A park with a family" />
		<!-- <img src="/images/park.png" alt="A park with a bench and trees" />
	</div>
	<div class="family">
		<img src="/images/full.png" alt="A family with a child" /> -->
	</div>

	<div class="container">
		<div class="text">
			<div style="--grid-area: title;" data-gu-name="title" class="line title">
				<p>{copy.title}</p>
			</div>
			<div
				style="--grid-area: headline;"
				data-gu-name="headline"
				class="line headline"
			>
				<p>{copy.headline}</p>
			</div>
			<div style="--grid-area: dek;" data-gu-name="dek" class="line dek">
				<p>{copy.dek}</p>
			</div>
			<div
				style="--grid-area: byline;"
				data-gu-name="byline"
				class="line byline"
			>
				<p>{copy.byline}</p>
			</div>
			<div style="--grid-area: date;" data-gu-name="date" class="line date">
				<p>{copy.date}</p>
			</div>
		</div>
	</div>
</div>

<style>
	.landing {
		position: relative;
		width: 100vw;
		height: 100vh;
		flex-shrink: 0;
		background: #4a5668;
		display: flex;
		justify-content: center;
		align-items: center;
		overflow: hidden;
	}
	.image-container {
		position: absolute;
		/* top: 0;
		left: 0; */
		width: 100%;
		height: 100%;
		min-height: 1024px;
		min-width: 1440px;
		object-fit: contain;
	}
	.image-container img {
		width: 100%;
		height: 100%;
		object-fit: contain;
		opacity: 0.66;
	}
	.container {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: flex;
		justify-content: flex-start;
		align-items: flex-start;
		pointer-events: none;
	}
	.text {
		font-family: "Sansita", sans-serif;
		color: white;
		display: grid;
		gap: 0;
		text-align: left;
		margin-left: 10%;
		margin-top: 8%;
		margin-right: 10%;
	}
	.line {
		background: rgba(0, 0, 0, 1);
		padding: 0;
	}
	.line p {
		margin: 0.3rem;
	}

	.line.title {
		/* width: 90%; */
		flex-shrink: 1;
		font-size: 2.5vw;
		color: #fff;
		-webkit-text-stroke-width: 2px;
		-webkit-text-stroke-color: #000;
		font-size: 48px;
		font-style: normal;
		font-weight: 800;
		line-height: normal;
		letter-spacing: 0.48px;
	}

	.line.headline {
		display: flex;
		/* width: 1064px; */
		min-width: 398px;
		flex-direction: column;
		justify-content: center;
		flex-shrink: 0;
		-webkit-text-stroke-width: 1px;
		-webkit-text-stroke-color: #000;
		font-size: 2rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
		letter-spacing: 0.36px;
	}

	.line.dek {
		display: flex;
		/* width: 1064px; */
		flex-direction: column;
		justify-content: center;
		flex-shrink: 0;
		color: #fff;
		-webkit-text-stroke-width: 0.8px;
		-webkit-text-stroke-color: #000;
		font-size: 1.3rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
		letter-spacing: 0.2px;
	}

	.line.byline {
		display: flex;
		/* width: 567px; */
		flex-direction: column;
		justify-content: center;
		flex-shrink: 0;
		color: #54095b;
		font-size: 1.2rem;
		font-style: italic;
		font-weight: 400;
		line-height: normal;
		letter-spacing: 0.3px;
	}
	.line.date {
		font-size: 0.8rem;
		font-style: italic;
		color: #648840;
		font-weight: 400;
		line-height: normal;
		letter-spacing: 0.23px;
	}
</style>
