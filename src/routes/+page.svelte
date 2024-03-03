<script lang="ts">
	import marlo from '$lib/images/marlo_head.png';

	let birthday = new Date(2023, 10, 23);
	let diffTime = Math.abs(Date.now() - birthday.getTime());
	let days = Math.floor(diffTime / (1000 * 60 * 60 * 24));
	let weeks = Math.floor(days / 7);
	let months = Math.floor(days / 30);
</script>

<div class="container">
	<div class="header">
		<h2>Marlo is...</h2>
	</div>
	<h2><span class="timer">{days}</span> days</h2>
	<h2><span class="timer">{weeks}</span> weeks</h2>
	<h2><span class="timer">{months}</span> months</h2>
	<div class="marlo">
		<img src={marlo} alt="marlo" />
	</div>
</div>

<style>
	:global(body) {
		background: rgb(2, 0, 36);
		background: linear-gradient(0deg, rgba(2, 0, 36, 1) 0%, rgba(4, 4, 61, 1) 100%);
		color: rgba(255, 255, 255, 0.937);
		height: 100vh;
		font-family: Acme;
	}

	.container {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		min-height: 100vh;
	}

	.header {
		position: absolute;
		width: 100%;
		top: 0px;
		left: 50%;
		text-align: center;
		transform: translate(-50%, 80px);
		font-size: 3em;
		text-shadow: 3px 3px 5px black;
	}

	.timer {
		font-size: 2em;
		font-weight: bold;
		margin-right: 0.1em;
	}

	.marlo {
		position: absolute;
		bottom: 0;
		left: 50%;
		transform: translate(-50%, 15px);
	}

	.marlo img {
		width: 300px;
	}
</style>
