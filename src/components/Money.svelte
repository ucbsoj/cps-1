<script>
	import copy from "$data/copy.json";
</script>

<!-- Small Info Square -->
<div class="info-box">
	<p>
		In the 2024–25 fiscal year, California allocated approximately $9.8 billion
		in total funding expenditures for its child welfare system, which
		encompasses services such as foster care, adoption assistance, kinship care,
		and family support programs.
	</p>
</div>

<div class="funding-container">
	<div class="image-box">
		<div class="fund-box">
			<img src="./main/fed.png" alt="federal" />
			<p class="fund-label">Tax revenu from Federal Government</p>
		</div>

		<div class="fund-box">
			<img src="./main/state.png" alt="state" />
			<p class="fund-label">Tax revenu from State Government</p>
		</div>

		<div class="fund-box">
			<img src="./main/county.png" alt="county" />
			<p class="fund-label">Allocations from County programs</p>
		</div>
	</div>

	<div class="merge-box"></div>

	<div class="main-arrow"></div>

	<div class="pie-chart-box">
		<iframe
			title="Funding Pie Chart"
			src="https://datawrapper.dwcdn.net/i1baC/1/"
			frameborder="0"
			width="650"
			height="700"
			scrolling="no"
			style="margin-top:20px;"
		>
		</iframe>
	</div>
</div>

<style>
	.money {
		background-color: #4a5668;
		color: #fff;
		font-family: "Sansita", sans-serif;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	/* Styling for the small info square */

	.info-box {
		width: 800px;
		padding: 20px;
		margin: 20px auto;
		background-color: #f2f2f200;
		border: 5px solid #648840;
		border-radius: 0px;
		text-align: center;
		font-size: 16px;
	}

	.funding-container {
		width: 80%;
		margin: 0 auto;
		padding: 20px;
		border: 5px solid #648840;
		border-radius: 0;
		text-align: center;
		font-size: 16px;
	}

	.image-box {
		display: flex;
		justify-content: center;
		align-items: flex-start;
		gap: 100px;
		margin-bottom: 10px;
	}

	.image-box img {
		width: 170px; /* control size */
		height: auto;
		object-fit: contain; /* keeps image looking good */
	}

	.fund-box {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 150px;
	}

	.merge-box {
		position: relative;
		border-left: 6px solid #648840;
		border-right: 6px solid #648840;
		border-bottom: 6px solid #648840;
		height: 80px;
		width: 50%;
		margin: 0 auto;
	}

	.merge-box::before {
		content: "";
		position: absolute;
		top: 0;
		bottom: 0;
		left: 50%;
		width: 6px;
		background-color: #648840;
		transform: translateX(-50%);
	}

	.main-arrow {
		width: 6px;
		height: 100px;
		background-color: #648840;
		margin: 0 auto;
		position: relative;
		margin-bottom: 30px;
	}

	.main-arrow::after {
		content: "";
		position: absolute;
		top: 100%;
		left: 50%;
		transform: translateX(-50%);
		border-left: 6px solid transparent;
		border-right: 6px solid transparent;
		border-top: 10px solid #648840;
	}

	.pie-chart-box {
		margin-top: 40px;
		padding-top: 20px;
		display: flex;
		justify-content: center;
		width: 100%;
		overflow: hidden;
	}
</style>
