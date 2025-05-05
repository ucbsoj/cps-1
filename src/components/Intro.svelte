<script>
	import copy from "$data/copy.json";
	import { packSiblings } from "d3";
	import Phone from "./Phone.svelte";
</script>

<div class="content">
	<div class="writing">
		<p class="preface">{copy.preface}</p>
		<div class="pic">
			<img
				src="./main/house.svg"
				alt="A house with a family standing inside."
			/>
		</div>
		<div class="text1">
			<p class="family-together">
				{copy.familytogether}
			</p>
			<p>{copy.book}</p>
			<p>{copy.sustain}</p>
			<p>{copy.un}</p>
		</div>
		<Phone />
		<div class="text2">
			<p>{copy.phone}</p>
			<p>{copy.mandated}</p>
			<p>{copy.repercussions}</p>
			<p>{copy.neglect}</p>
			<p>{copy.negligent}</p>
			<p>{copy.numbers}</p>
		</div>
		<img
			src="./main/maltreatment.png"
			alt="A bar chart showing the almost 74% of children in the child welfare system are there because of poverty."
		/>
	</div>
	<!-- <div class="pic">
		<img src="./main/letters.svg" alt="A teacher playing with a child." />
	</div>
	<p class="teacher">
		{copy.teacher}
	</p> -->
	<h1>Let's follow the money.</h1>
</div>

<style>
	h1 {
		margin-top: 200px;
		color: #fff;
		text-align: center;
		font-family: "Sansita", sans-serif;
	}
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
		margin-left: 30%;
		margin-right: 30%;
		margin-top: 50px;
		align-items: center;
		justify-content: center;
		display: flex;
		flex-direction: column;
		text-align: center;
	}
	.preface {
		font-size: 0.8rem;
		color: #fff;
		text-align: center;
		margin-bottom: 1rem;
		width: 70%;
		font-style: italic;
		align-items: center;
	}
	.teacher {
		margin-left: 20%;
		margin-right: 20%;
		align-items: center;
		justify-content: center;
		display: flex;
		flex-direction: column;
	}
	p {
		align-items: center;
	}
	.family-together {
		color: #fff;
		text-align: center;
	}

	p {
		margin-top: 30px;
	}
</style>
