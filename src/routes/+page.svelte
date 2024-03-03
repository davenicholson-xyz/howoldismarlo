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
	<svg xmlns="http://www.w3.org/2000/svg" width="2.4em" height="2.4em" viewBox="0 0 24 24"
		><path
			fill="currentColor"
			d="M8 14a3 3 0 0 1-3 3a3 3 0 0 1-3-3c0-.77.29-1.47.76-2c-.47-.53-.76-1.23-.76-2a3 3 0 0 1 3-3a3 3 0 0 1 3 3c1.33.08 2.67.17 4 .17s2.67-.09 4-.17a3 3 0 0 1 3-3a3 3 0 0 1 3 3c0 .77-.29 1.47-.76 2c.47.53.76 1.23.76 2a3 3 0 0 1-3 3a3 3 0 0 1-3-3c-1.33-.08-2.67-.17-4-.17s-2.67.09-4 .17"
		/></svg
	>
	<h2><span class="timer">{weeks}</span> weeks</h2>
	<svg xmlns="http://www.w3.org/2000/svg" width="2.4em" height="2.4em" viewBox="0 0 24 24"
		><path
			fill="currentColor"
			d="M8 14a3 3 0 0 1-3 3a3 3 0 0 1-3-3c0-.77.29-1.47.76-2c-.47-.53-.76-1.23-.76-2a3 3 0 0 1 3-3a3 3 0 0 1 3 3c1.33.08 2.67.17 4 .17s2.67-.09 4-.17a3 3 0 0 1 3-3a3 3 0 0 1 3 3c0 .77-.29 1.47-.76 2c.47.53.76 1.23.76 2a3 3 0 0 1-3 3a3 3 0 0 1-3-3c-1.33-.08-2.67-.17-4-.17s-2.67.09-4 .17"
		/></svg
	>
	<h2><span class="timer">{months}</span> months</h2>
	<div class="marlo">
		<img src={marlo} alt="marlo" />
	</div>
</div>

<style>
	:global(body) {
		background: rgb(2, 0, 36);
		background-color: #92c4e8;
		background-image: linear-gradient(to right, #141e30, #243b55);

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

	h2 {
		text-shadow: 2px 2px 5px black;
	}

	.header {
		position: absolute;
		width: 100%;
		top: 0px;
		left: 50%;
		text-align: center;
		transform: translate(-50%, 40px);
		font-size: 3em;
		text-shadow: 3px 3px 5px black;
		color: goldenrod;
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
