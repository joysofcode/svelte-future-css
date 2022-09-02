<svelte:head>
	<title>Future CSS</title>
</svelte:head>

<h1>Use Future CSS Today 😎</h1>

<style lang="postcss">
	:global(body) {
		height: 100vh;
		display: grid;
		place-content: center;
		margin: 0;
		color: hsl(220 20% 98%);
		background-color: hsl(220 20% 14%);
		font-family: sans-serif;
	}

	/* Nesting */

	@layer base {
		h1 {
			color: white;
			transition: transform 10s ease;

			&:hover {
				transform: rotate(2turn);
			}
		}
	}

	/* Layers */

	@layer typography {
		h1 {
			font-size: 3rem;
			color: aquamarine;
		}
	}

	/* Media queries */

	@custom-media --narrow (max-width: 400px);

	@media (--narrow) {
		h1 {
			color: tomato;
		}
	}

	@media (width < 200px) {
		h1 {
			color: palegreen;
		}
	}
</style>
