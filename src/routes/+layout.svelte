<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import '../app.css';

	let navIsOpen = false;
</script>

<Nav {navIsOpen} />
<header>
	<nav>
		<div class="logo">
			<a href="/">
				<img src="yvenoz-logo.svg" alt="yvenoz services logo">
			</a>
		</div>
		<ul>
			<li class="contact ">
				<a href="/#contacts"> CONTACTS </a>
			</li>
			<li>
				<button on:click={() => (navIsOpen = !navIsOpen)}>
					<span>MENU</span>

					<span class="hamberger">
						<span class:active-one={navIsOpen} />
						<span />
						<span class:active-three={navIsOpen} />
					</span>
				</button>
			</li>
		</ul>
	</nav>
</header>

<main>
	<slot />
</main>

<footer>
	<Footer />
</footer>

<style>
	header {
		width: 100%;
		padding: 1.5vw 3vw;
		position: fixed;
		top: 0;
		z-index: 50;
		color: var(--bg);
		/* background-color: var(--bg); */
		mix-blend-mode: difference;
		background-color: transparent;
		& nav {
			width: 100%;
			display: flex;
			justify-content: space-between;
			align-items: center;
		}

		& ul {
			display: flex;
			align-items: center;
			gap: 3rem;
		}

		& button {
			display: flex;
			align-items: center;
			justify-content: center;
			gap: 3rem;
			font-size: 1.8rem;
			cursor: pointer;
			height: 3rem;
			padding: 0 2rem;
			color: var(--bg);
		}

		& .hamberger {
			position: relative;
			width: 30px;
			height: 60%;
		}

		& .hamberger > span {
			display: block;
			height: 2px;
			width: 100%;
			background-color: var(--bg);
			position: absolute;
			transition: transform 0.5s ease-out;
		}

		& .hamberger span:nth-child(1) {
			top: 0;
		}
		& .hamberger span:nth-child(2) {
			top: 50%;
			transform: translateY(-50%);
		}
		& .hamberger span:nth-child(3) {
			bottom: 0;
		}
	}

	.active-one {
		transform: translateX(7px);
	}
	.active-three {
		transform: translateX(-7px);
	}

	.logo {
		mix-blend-mode: exclusion;
	}

	nav ul {
		mix-blend-mode: de;
	}


	@media (width < 600px) {
		.contact {
			display: none;
		}
	}
</style>
