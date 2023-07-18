<script>
	import '../styles.css';
</script>

<svelte:head>
	<title>Beat Leader</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="authContainer">
	<p class="authText">
		Click Authorize to login to Beat Leader
	</p>
	<button class="authButton">
		Authorize
	</button>
</div>


<style>
	.authContainer {
		position: fixed;
		top: 30%;
		width: 858px;
		height: 312px;
		display: flex;
		flex-direction: column;
		align-items: center;

		border-radius: 30px;
		background: #252525;
		box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
	}

	.authText {
		color: #FFF;
		text-align: center;
		font-family: Heebo;
		font-size: 30px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
	}

	.authButton {
		border: none;
		width: 450px;
		height: 85px;
		flex-shrink: 0;
		margin-top: 40px;

		border-radius: 20px;
		background: #B27C66;
		box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);

		color: #FFF;
		text-align: center;
		font-family: Heebo;
		font-size: 50px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
	}
</style>