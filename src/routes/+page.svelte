<div class="nav-bar">
	<div class="title">
		Daniel <span class="highlighted">Villavicencio</span>
	</div>
	<div class="container-link">
		<a href="/projects"> Projects </a>
	</div>
	<div class="container-link">
		<a href="/timeline"> Bio </a>
	</div>
	<div class="container-link">
		<a href="/contact"> Source </a>
	</div>
	<div class="container-link">
		<a href="/resume"> Resume </a>
	</div>
</div>

<style>
	/* :global(body) {
		background: #282c32
	} */
	body {
		background-color: #282c32
	}
	@import url("https://fonts.googleapis.com/css2?family=Noto+Sans:wght@300&family=PT+Sans+Narrow&family=Plus+Jakarta+Sans:ital,wght@0,400;1,300&display=swap");
	.nav-bar {
		background-color: rgba(132, 139, 200, 0.18);
		margin-bottom: 1.5rem;
		padding: 10px;
		height: 40px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: "Plus Jakarta Sans", "PT Sans Narrow", "Noto Sans",
			sans-serif;
	}
	.nav-bar .container-link {
		display: flex;
		border-radius: 0.25rem;
		justify-content: center;
		align-items: center;
		width: 80px;
		height: 30px;
		cursor: pointer;
	}
	.nav-bar .container-link a {
		text-decoration: none;
		box-sizing: border-box;
		margin: 0;
		color: #677483;
		font-size: 15px;
	}
	.nav-bar .container-link:hover {
		box-shadow: 0 0 1rem rgba(0, 0, 0, 0.18);
		border-radius: 15px;
		transition: all 0.25s ease;
	}
	.nav-bar .title {
		margin: 1.5rem;
		color: #677483;
	}
	.highlighted {
		color: rgb(255, 136, 0);
	}
</style>
