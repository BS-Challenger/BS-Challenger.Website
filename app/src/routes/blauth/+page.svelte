<script>
	import '../styles.css';
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	onMount(async () => {
		const url = $page.url;
		document.cookie = "code=" + url.searchParams.get('code') + "; SameSite=None; Secure";

		return {
			url
		};
	});
	const debug = true;
	let targetURL = "";
	if(!debug) {
		targetURL = "https://bschallenger.xyz"
	}
	else
	{
		targetURL = "http://localhost:8080"
	}
</script>

<svelte:head>
	<title>Beat Leader</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="authContainer">
	<p class="authText">
		Click Authorize to login to Beat Leader
	</p>
	<button class="authButton" on:click={()=>window.open("https://api.beatleader.xyz/oauth2/authorize?client_id=BSChallengerClientID&response_type=code&redirect_uri=" + targetURL + "/beatleader-callback&scope=profile",'_blank')}>
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
		transition-duration: 0.2s;
	}

	.authButton:hover {
		background: #d79c88;
		transition-duration: 0.2s;
		cursor: pointer;
		transform: rotateX(15deg);
	}
</style>