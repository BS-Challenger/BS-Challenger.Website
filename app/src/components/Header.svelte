<header>
	<nav>
		<div class="header">
			<img class="icon" src="/favicon.png"/>
			<p style="font-size: 25px">
				BS Challenger
			</p>
		</div>
	</nav>
</header>

<style>
	p {
		color: #FFF;
		font-family: Montserrat Alternates;
		font-size: 35px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
		margin-left: 20px;
	}

	.icon {
		width: 70px;
		height: 70px;
		margin: 5px;
		flex-shrink: 0;
		border-radius: 20px;
		border: 4px solid #CAA8F5;
		background: url("/favicon.png"), lightgray 50% / cover no-repeat;

	}

	.header {
		margin-top: -8px;
		width: 90%;
		height: 10%;
		flex-shrink: 0;

		display: flex;
		flex-direction: row;

		border-radius: 0px 0px 25px 25px;
		border: 8px solid #592E83;
		background: linear-gradient(90deg, #9984D4 0%, #CAA8F5 100%);
		box-shadow: 0px 4px 4px 4px rgba(0, 0, 0, 0.25);
		transition: transform 300ms linear;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}
</style>
