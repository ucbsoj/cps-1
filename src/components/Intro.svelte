<script>
	import copy from "$data/copy.json";
</script>

<div class="content">
	<div class="writing">
		<p class="preface">{copy.preface}</p>
		<div class="pic">
			<img src="/main/house.svg" alt="A house with a family standing inside." />
		</div>
		<p class="family-together">{copy.familytogether}</p>
	</div>
</div>

<style>
	.pic {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100%;
		width: 100%;
	}
	.pic img {
		width: 300px;
		height: auto;
		color: black;
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
	.preface {
		font-size: 0.8rem;
		color: #fff;
		text-align: center;
		margin-bottom: 1rem;
		width: 70%;
		font-style: italic;
	}
</style>
