<script>
	import copy from "$data/copy.json";
</script>

<h1>So how does this system work?</h1>
<i class="Phone is-animating"></i>

<style>
	h1 {
		margin-top: 200px;
	}
	body {
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 0;
		width: 100vw;
		height: 100vh;
		background-color: #ecf0f1;
	}

	.Phone {
		margin-top: 20%;
		position: relative;
		display: block;
		margin: 0;
		width: 1em;
		height: 1em;
		font-size: 20vmin;
		background-color: #45921f82;
		border-radius: 0.5em;
		box-shadow:
			0 0 0 0em rgba(#00000044, 0),
			0em 0.05em 0.1em rgba(#000000, 0.2);
		transform: translate3d(0, 0, 0) scale(1);
	}

	.Phone::before,
	.Phone::after {
		position: absolute;
		content: "";
	}

	.Phone::before {
		top: 0;
		left: 0;
		width: 1em;
		height: 1em;
		background-color: rgba(#fff, 0.1);
		border-radius: 100%;
		opacity: 1;
		transform: translate3d(0, 0, 0) scale(0);
	}

	.Phone::after {
		top: 0.25em;
		left: 0.25em;
		width: 0.5em;
		height: 0.5em;
		background: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTYuNiAxMC44YzEuNCAyLjggMy44IDUuMSA2LjYgNi42bDIuMi0yLjJjLjMtLjMuNy0uNCAxLS4yIDEuMS40IDIuMy42IDMuNi42LjUgMCAxIC40IDEgMVYyMGMwIC41LS41IDEtMSAxLTkuNCAwLTE3LTcuNi0xNy0xNyAwLS42LjQtMSAxLTFoMy41Yy41IDAgMSAuNCAxIDEgMCAxLjIuMiAyLjUuNiAzLjYuMS40IDAgLjctLjIgMWwtMi4zIDIuMnoiIGZpbGw9IiNmZmZmZmYiLz48L3N2Zz4=);
		background-position: 50% 50%;
		background-repeat: no-repeat;
		background-size: cover;
		transform: translate3d(0, 0, 0);
	}

	.Phone.is-animating {
		animation: phone-outer 3000ms infinite;

		&::before {
			animation: phone-inner 3000ms infinite;
		}

		&::after {
			animation: phone-icon 3000ms infinite;
		}
	}

	@keyframes phone-outer {
		0% {
			transform: translate3d(0, 0, 0) scale(1);
			box-shadow:
				0 0 0 0em rgba(#3498db, 0),
				0em 0.05em 0.1em rgba(#000000, 0.2);
		}
		33.3333% {
			transform: translate3d(0, 0, 0) scale(1.1);
			box-shadow:
				0 0 0 0em rgba(#3498db, 0.1),
				0em 0.05em 0.1em rgba(#000000, 0.5);
		}
		66.6666% {
			transform: translate3d(0, 0, 0) scale(1);
			box-shadow:
				0 0 0 0.5em rgba(#3498db, 0),
				0em 0.05em 0.1em rgba(#000000, 0.2);
		}
		100% {
			transform: translate3d(0, 0, 0) scale(1);
			box-shadow:
				0 0 0 0em rgba(#3498db, 0),
				0em 0.05em 0.1em rgba(#000000, 0.2);
		}
	}

	@keyframes phone-inner {
		0% {
			opacity: 1;
			transform: translate3d(0, 0, 0) scale(0);
		}
		33.3333% {
			opacity: 1;
			transform: translate3d(0, 0, 0) scale(0.9);
		}
		66.6666% {
			opacity: 0;
			transform: translate3d(0, 0, 0) scale(0);
		}
		100% {
			opacity: 0;
			transform: translate3d(0, 0, 0) scale(0);
		}
	}

	@keyframes phone-icon {
		0% {
			transform: translate3d(0em, 0, 0);
		}
		2% {
			transform: translate3d(0.01em, 0, 0);
		}
		4% {
			transform: translate3d(-0.01em, 0, 0);
		}
		6% {
			transform: translate3d(0.01em, 0, 0);
		}
		8% {
			transform: translate3d(-0.01em, 0, 0);
		}
		10% {
			transform: translate3d(0.01em, 0, 0);
		}
		12% {
			transform: translate3d(-0.01em, 0, 0);
		}
		14% {
			transform: translate3d(0.01em, 0, 0);
		}
		16% {
			transform: translate3d(-0.01em, 0, 0);
		}
		18% {
			transform: translate3d(0.01em, 0, 0);
		}
		20% {
			transform: translate3d(-0.01em, 0, 0);
		}
		22% {
			transform: translate3d(0.01em, 0, 0);
		}
		24% {
			transform: translate3d(-0.01em, 0, 0);
		}
		26% {
			transform: translate3d(0.01em, 0, 0);
		}
		28% {
			transform: translate3d(-0.01em, 0, 0);
		}
		30% {
			transform: translate3d(0.01em, 0, 0);
		}
		32% {
			transform: translate3d(-0.01em, 0, 0);
		}
		34% {
			transform: translate3d(0.01em, 0, 0);
		}
		36% {
			transform: translate3d(-0.01em, 0, 0);
		}
		38% {
			transform: translate3d(0.01em, 0, 0);
		}
		40% {
			transform: translate3d(-0.01em, 0, 0);
		}
		42% {
			transform: translate3d(0.01em, 0, 0);
		}
		44% {
			transform: translate3d(-0.01em, 0, 0);
		}
		46% {
			transform: translate3d(0em, 0, 0);
		}
	}
	p {
		margin-left: 20%;
		margin-right: 20%;
	}
</style>
