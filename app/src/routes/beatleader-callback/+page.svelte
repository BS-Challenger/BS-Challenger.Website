<script>
	import '../styles.css';
	import Check from 'carbon-icons-svelte/lib/Checkmark.svelte'
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	onMount(async () => {
		const url = $page.url;
		const blToken = url.searchParams.get('code');
		const genToken = document.cookie
				.split("; ")
				.find((row) => row.startsWith("code="))
				?.split("=")[1];
		console.log(genToken);
		console.log(blToken);
		console.log(JSON.stringify({
			GeneratedCode: genToken,
			BLCode: blToken
		}));

		let obj = {
			GeneratedCode: genToken,
			BLCode: blToken
		}

		const response = (await fetch('http://localhost:8081/BeatLeaderAuthenticate/BLAuthenticate', {
			method: 'POST',
			mode: "no-cors",
			headers: {
				'Accept': 'application/json; charset=utf-8',
				'Content-Type': 'application/json; charset=utf-8'
			},
			body: JSON.stringify(obj),
		})).then(response => response.json())
				.then(response => console.log(JSON.stringify(response)))

		console.log(response);

		return {
			url
		};
	});
</script>

<svelte:head>
	<title>Authorized</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="authorizedContainer">
	<div class="texts">
		<Check size={64} style="margin-right: 10px; color: green; " class="check"/>
		<p class="authorizedText">
			Authorized
		</p>
	</div>
	<p class="authorizedSubText">
		... You can return to your game now :)
	</p>
</div>


<style>
	.authorizedContainer {
		position: fixed;
		top: 30%;
		width: 40%;
		height: 312px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		left: 50%;
		margin-left: -20%;

		border-radius: 30px;
		background: #252525;
		box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
	}

	.authorizedText {
		color: #FFF;
		text-align: center;
		font-family: Heebo;
		font-size: 50px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
		margin: 0px;
		align-self: center;
	}

	.authorizedSubText {
		color: #FFF;
		text-align: center;
		font-family: Heebo;
		font-size: 20px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
	}

	.texts {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
</style>