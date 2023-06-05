<script lang="ts">
	import {theme} from "../stores.ts";
	import {browser} from "$app/environment";

	theme.subscribe(newTheme => {
		if(!browser)
			return;
		if(newTheme === "light") {
			document.body.classList.add("light");
		} else {
			document.body.classList.remove("light");
		}
	});
</script>

<svelte:head>
	<title>Name</title>
	<meta name="description" content="" />
</svelte:head>

<section class="container">
	<div class="hero">
		<div class="main">
			<h1>Lorem ipsum deloris<br /> Shakespeare</h1>
			<br />
			<button class="gradient-button">
				Start Now
			</button>
		</div>
	</div>
</section>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,300;0,400;0,700;1,400&display=swap');

	h1 {
		font-size: 40px;
	}

	.hero {
		height: 100vh;
	}

	.gradient-button {
		background: linear-gradient(to right,#bd00ff 0%,#6100ff 51%,#bd00ff 100%);
		background-size: 200% auto;
		color: white;
		font-size: 24px;
		margin: 10px;
		padding: 16px 20px;

		&:hover {
			background-position: right center;
		}
	}

	.main {
		margin-top: 18%;
	}

	:root {
		--text-color: white;
		--theme-font: 'IBM Plex Mono', monospace;
		--theme-background: #070707;
		--theme-dark: #2a2a2a;
		--theme-semi-dark: #b71010;
		--theme-light: #f03ed5;
		--theme-extra-light: #00D4FF;
	}

	:global {
		* {
			margin: 0;
			padding: 0;
			font-family: var(--theme-font);
		}

		body {
			background-color: var(--theme-background);
			transition: background-color ease-in 1s;
		}

		body.light {
			--text-color: black;
			--theme-background: white;
		}

		h1, h2, h3, h4, h5, h6, p, span {
			display: inline-block;
			color: var(--text-color);
		}

		button {
			display: inline-flex;
			justify-content: center;
			align-items: center;
			border-radius: 50px;
			border: none;
			padding: 6px 8px;
			color: #a8a8a8;
			font-weight: bold;

			background: linear-gradient(to left, transparent 50%, var(--theme-dark) 50%) right;
			background-size: 200%;
			transition: .5s ease-out;

			&:hover {
				cursor: pointer;
				background-position: left;
			}

			&:active {
				filter: brightness(60%);
			}
		}
	}
</style>
