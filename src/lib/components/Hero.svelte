<script lang="ts">
	import { onMount } from 'svelte';
	import Btn from './btn.svelte';
	import { animate, stagger } from 'motion';

	let bigText = `Expérience de contrôle transparent
 avec nos solutions d’automatisation`.split(' ');

	const imgs = ['/hero/hero1.webp', '/hero/hero2.webp', '/hero/hero3.webp', '/hero/hero4.webp'];

	onMount(() => {
		const slides = [...document.querySelectorAll('#accueil .slide')]

		animate(slides, {y: [200, 0]}, {duration: 1, easing: 'ease-out', delay: stagger(0.1)})

		animate('#accueil .title p', {opacity: [0, 1]}, {duration: 0.5, easing: "ease-in-out", delay: 0.7}, )
		animate('#accueil .btn', {opacity: [0, 1], y:[10, 0]}, {duration: 0.5, easing: "ease-in-out", delay: 0.8}, )
		animate('#accueil figure', {scale: [0.8, 1], opacity:[0, 1]}, {duration: 1.5, delay: stagger(0.2), easing: "ease-in-out"}, )
	})
</script>

<section id="accueil">
	<div class="title">
		<h1>
			<span>
				<span class="slide">Expérience de contrôle transparent</span>
			</span>

			<br />
			<span>
				<span class="slide">avec nos solutions </span>
			</span>
			<br />
			<span>
				<span class="slide">d’automatisation</span>
			</span>
		</h1>
		<div class="para">
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem, enim! Aspernatur quos adipisci
				dolor laboriosam itaque quibusdam nihil voluptas in pariatur, commodi rem, fuga odit
				voluptatibus unde velit quaerat recusandae.
			</p>
		</div>
	</div>
	<a  class="btn" href="/#contacts">
		<Btn />
	</a>
	<div class="imgs">
		{#each imgs as img}
			<figure>
				<img src={img} alt="Door " />
			</figure>
		{/each}
	</div>
</section>

<style>
	section {
		min-height: 100dvh;
		padding: 22rem 5vw 3rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 3.2rem;
	}

	.title {
		width: 100%;
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 3.2rem;
	}

	h1 {
		font-size: clamp(2.5rem, 4vw + 0.1rem, 10rem);
		text-transform: uppercase;
		/* display: flex;
		flex-wrap: wrap; */
		line-height: 80%;
		flex-shrink: 2;
		position: relative;
		/* gap: 15px; */
	}

	.para {
		position: absolute;
		right: 5%;
		max-width: 50rem;
		top: 40%;
		/* background-color: red; */
	}

	.imgs {
		margin-top: 6rem;
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 2rem;
	}

	figure {
		border-radius: 20px;
		position: relative;
	}

	img {
		width: 100%;
		height: 100%;
		border-radius: 20px;
		object-fit: cover;
	}

	.imgs figure:nth-child(2),
	.imgs figure:nth-child(4) {
		top: 20px;
	}


	h1 > span {
		overflow: hidden;
		display: inline-block;
		/* height: max-content; */
	}


	.slide {
		/* background-color: red; */
		display: inline-block;
	}

	@media (width < 1322px) {
		.para {
			right: 0;
		}

		.para p {
			font-size: 14px;
		}

		h1 {
			font-size: clamp(2rem, 3vw + 0.1rem, 10rem);
		}

		.title {
			align-items: flex-start;
		}
	}


	@media (width < 950px) {
		.para {
			position: static;
		}

		.para p {
			text-align: center;
		}
		.title {
			align-items: center;
		}

		h1 {
			text-align: center;
		}

		section {
			padding-top: 15rem;
		}
	}
</style>
