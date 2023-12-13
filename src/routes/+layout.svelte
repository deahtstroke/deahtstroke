<div class="nav-bar">
	<div class="container-link">
		<a href="/">
            <span class="material-symbols-outlined">home</span>
			Home
		</a>
	</div>
	<div class="container-link">
		<a href="/projects">
			<span class="material-symbols-outlined"> description </span>
			Projects
		</a>
	</div>
	<div class="container-link">
		<a href="/bio">
			<span class="material-symbols-outlined"> person_book </span>
			About
		</a>
	</div>
	<div class="container-link">
		<a href="/resume">
			<span class="material-symbols-outlined"> description </span>
			Resume
		</a>
	</div>
</div>

<slot/>

<style>
	@import url("https://fonts.googleapis.com/css2?family=Noto+Sans:wght@300&family=PT+Sans+Narrow&family=Plus+Jakarta+Sans:ital,wght@0,400;1,300&display=swap");
	:global(body) {
		background: #282c32;
        font-family: "Plus Jakarta Sans", "Noto Sans", sans-serif;
        color: rgb(231, 231, 231);
	}
	.nav-bar {
		background-color: rgba(132, 139, 200, 0.18);
		margin-bottom: 1.5rem;
		gap: 1.8rem;
		padding: 10px;
		height: 40px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.nav-bar .container-link {
		display: flex;
		border-radius: 0.25rem;
		justify-content: center;
		align-items: center;
		width: 100px;
		height: 33px;
		cursor: pointer;
	}
	.nav-bar .container-link a {
		display: flex;
		align-items: center;
		justify-content: baseline;
		text-decoration: none;
		box-sizing: border-box;
		gap: 0.5rem;
		color: rgb(231, 231, 231);
		font-size: 15px;
        position: relative;
	}
	.nav-bar .container-link:hover {
		background-color: rgba(132, 139, 200, 0.18);
		border-radius: 4px;
		transition: all 0.3s ease;
	}
	.nav-bar .title a {
		font-size: 18px;
		color: rgb(231, 231, 231);
        text-decoration: none;
	}
    .nav-bar .title a:hover {
        text-decoration: none;
	}
</style>
