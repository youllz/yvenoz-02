<script lang="ts">
	import Btn from './btn.svelte';

	let bigText = `Expérience de contrôle transparent
 avec nos solutions d’automatisation`.split(' ');
</script>

<section>
	<div class="text-container">
		<h1>
			{#each bigText as item}
				<span><span>{item} </span></span>
			{/each}
		</h1>
		<p>
			Votre partenaire en materiels d'automatismes pour portail, porte de garage, barriere levante
			de parking, porte automatique pietonne et pieces detachees
		</p>
		<Btn />
	</div>
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
			font-size: clamp(14px, 1.8rem, 2rem);
		}
	}
</style>
