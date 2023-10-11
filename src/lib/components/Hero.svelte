<script lang="ts">
	import Btn from './btn.svelte';

	let bigText = `Expérience de contrôle transparent
 avec nos solutions d’automatisation`.split(' ');

	const imgs = ['/hero/hero1.webp', '/hero/hero2.webp', '/hero/hero3.webp', '/hero/hero4.webp'];
</script>

<section id="accueil">
	<div class="text-container">
		<h1>
			{#each bigText as item}
				<span><span>{item} </span></span>
			{/each}
		</h1>
		<p>
			Votre partenaire en matériels d'automatismes pour portail, porte de garage, barrière levante
			de parking, porte automatique piétonne et pièces détachées.
		</p>
		<Btn />
	</div>

	{#each imgs as img, idx}
		<figure class="hero-img{idx}">
			<img src={img} alt="Door" />
		</figure>
	{/each}
</section>

<style>
	section {
		width: 100%;
		height: 100dvh;
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	h1 {
		font-size: clamp(3rem, 5vw + 0.1rem, 7rem);
		text-align: center;
		display: flex;
		max-width: 80%;
		flex-wrap: wrap;
		gap: 13px;
		justify-content: center;
		align-items: center;
		letter-spacing: -2px;
		text-transform: uppercase;
	}

	h1 > span {
		overflow: hidden;
		color: var(--bg);
		mix-blend-mode: difference;
	}

	.text-container {
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 32px;
		flex-direction: column;

		& p {
			max-width: 45em;
			text-align: center;
			font-size: clamp(14px, 1.8vw + 0.1rem, 2rem);
		}
	}

	figure {
		position: absolute;
		height: 30vh;
		width: 20vw;
		z-index: -1;
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: contain;
	}

	.hero-img0 {
		top: 10%;
		left: 10%;
	}
	.hero-img1 {
		top: 10%;
		right: 10%;
	}
	.hero-img2 {
		bottom: 10%;
		right: 10%;
	}
	.hero-img3 {
		bottom: 10%;
		left: 10%;
	}
</style>
