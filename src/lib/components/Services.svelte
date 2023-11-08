<script lang="ts">
	import { animate, inView, timeline, type TimelineDefinition } from "motion";
	import { onMount } from "svelte";

	onMount(() => {

		const sequence: TimelineDefinition = [
			["#services .line", {scaleX: [0, 1]}, {duration: 0.8, easing: "ease-in-out"}],
			["#services h3", {y: [20, 0], opacity: [0, 1]}, {duration: 0.4, easing: "ease-in-out", at: '-0.4'}],
			["#services p", {opacity: [0, 1]}, {duration: 0.6, easing: "ease-in-out"}],
		]
		
		inView('#services', () => {
			timeline(sequence)
		})

		const cards = [...document.querySelectorAll('.timeline-container .card')]

		inView(cards[0], ({target}) => {
			animate(target.querySelector('p') as HTMLParagraphElement, 
			{opacity: [0, 1], y: [50, 0]},
			{duration: 0.8, easing: "ease-out", delay: 0.5}
			)
		})
		inView(cards[1], ({target}) => {
			animate(target.querySelector('p') as HTMLParagraphElement, 
			{opacity: [0, 1], y: [50, 0]},
			{duration: 0.8, easing: "ease-out", delay: 0.5}
			)
		})
		inView(cards[2], ({target}) => {
			animate(target.querySelector('p') as HTMLParagraphElement, 
			{opacity: [0, 1], y: [50, 0]},
			{duration: 0.8, easing: "ease-out", delay: 0.5}
			)
		})



	})
</script>



<section>
	<div class="container" id="services">
		<div class="container-left">
			<span class="line"/>
			<h3>SERVICES</h3>
		</div>
		<div class="container-right">
			<p>
				De l'installation et de la personnalisation à la maintenance et aux réparations, notre gamme
				de services est conçue pour vous fournir des solutions de bout en bout pour vos systèmes
				d'automatisation.
			</p>
		</div>
	</div>

	<div class="timeline-container">
		<div class="card">
			<div>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 36 36"
						><path
							fill="currentColor"
							d="m10.3 18.87l7 6.89a1 1 0 0 0 1.4 0l7-6.89a1 1 0 0 0-1.4-1.43L19 22.65V4a1 1 0 0 0-2 0v18.65l-5.3-5.21a1 1 0 0 0-1.4 1.43Z"
							class="clr-i-outline--alerted clr-i-outline-path-1--alerted"
						/><path
							fill="currentColor"
							d="M31 15.4V30H5V10h4.38a1 1 0 0 0 0-2h-4.3A2 2 0 0 0 3 10v20a2 2 0 0 0 2.08 2h25.84A2 2 0 0 0 33 30V15.4Z"
							class="clr-i-outline--alerted clr-i-outline-path-2--alerted"
						/><path
							fill="currentColor"
							d="M26.85 1.14L21.13 11a1.28 1.28 0 0 0 1.1 2h11.45a1.28 1.28 0 0 0 1.1-2l-5.72-9.86a1.28 1.28 0 0 0-2.21 0Z"
							class="clr-i-outline--alerted clr-i-outline-path-3--alerted clr-i-alert"
						/><path fill="none" d="M0 0h36v36H0z" /></svg
					>
				</span>
				<h2>
					<span>01</span>
					INSTALATION
				</h2>
			</div>
			<p>
				Avant de terminer l'installation, notre équipe propose une formation complète à votre
				personnel ou au personnel qui utilisera les systèmes d'automatisation. Nous voulons nous
				assurer que vous êtes à l’aise avec le fonctionnement et l’entretien des matériauxs
			</p>
		</div>
		<!--  -->
		<div class="card">
			<div>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32"
						><path
							fill="currentColor"
							d="m29.707 19.293l-3-3a1 1 0 0 0-1.414 0L16 25.586V30h4.414l9.293-9.293a1 1 0 0 0 0-1.414zM19.586 28H18v-1.586l5-5L24.586 23zM26 21.586L24.414 20L26 18.414L27.586 20zM20 13v-2h-2.142a3.94 3.94 0 0 0-.425-1.019l1.517-1.517l-1.414-1.414l-1.517 1.517A3.944 3.944 0 0 0 15 8.142V6h-2v2.142a3.944 3.944 0 0 0-1.019.425L10.464 7.05L9.05 8.464l1.517 1.517A3.94 3.94 0 0 0 10.142 11H8v2h2.142a3.94 3.94 0 0 0 .425 1.019L9.05 15.536l1.414 1.414l1.517-1.517a3.944 3.944 0 0 0 1.019.425V18h2v-2.142a3.944 3.944 0 0 0 1.019-.425l1.517 1.517l1.414-1.414l-1.517-1.517A3.94 3.94 0 0 0 17.858 13zm-6 1a2 2 0 1 1 2-2a2.002 2.002 0 0 1-2 2z"
						/><path
							fill="currentColor"
							d="M12 30H6a2.002 2.002 0 0 1-2-2V4a2.002 2.002 0 0 1 2-2h16a2.002 2.002 0 0 1 2 2v10h-2V4H6v24h6Z"
						/></svg
					>
				</span>
				<h2>
					<span>02</span>
					MAINTENANCE
				</h2>
			</div>
			<p>
				Notre processus de maintenance commence par des inspections régulières de vos systèmes
				d'automatisation. Nos techniciens qualifiés effectuent des évaluations approfondies pour
				identifier tout problème potentiel ou usure.
			</p>
		</div>
		<!--  -->
		<div class="card">
			<div>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
						><g
							fill="none"
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="1.5"
							><path
								d="m10.05 10.607l-7.07 7.07a2 2 0 0 0 0 2.83v0a2 2 0 0 0 2.828 0l7.07-7.072m4.315.365l3.878 3.878a2 2 0 0 1 0 2.828v0a2 2 0 0 1-2.828 0l-6.209-6.208M6.733 5.904L4.61 6.61L2.49 3.075l1.414-1.414L7.44 3.782l-.707 2.122Zm0 0l2.83 2.83"
							/><path
								d="M10.05 10.607c-.844-2.153-.679-4.978 1.061-6.718c1.74-1.74 4.95-2.121 6.717-1.06l-3.04 3.04l-.283 3.111l3.111-.282l3.04-3.041c1.062 1.768.68 4.978-1.06 6.717c-1.74 1.74-4.564 1.905-6.717 1.061"
							/></g
						></svg
					>
				</span>
				<h2>
					<span>03</span>
					REPARATION
				</h2>
			</div>
			<p>
				Notre engagement envers votre satisfaction s'étend au-delà de la réparation elle-même. Nous
				fournissons une assistance et des conseils après réparation.
			</p>
		</div>
	</div>
</section>

<style>
	section {
		width: 100%;
		min-height: 100dvh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		align-items: center;
		background-color: var(--secondary);
		padding-top: 15vw;
	}

	.container {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(33rem, 1fr));
		gap: 3rem;
		place-content: center;
		max-width: 100rem;
	}

	.container-left {
		& span {
			display: inline-block;
			width: 70%;
			height: 2px;
			background-color: var(--accent);
			transform-origin: left;
		}

		& h3 {
			margin-top: 0.5rem;
			color: var(--accent);
			font-size: 1.4rem;
		}
	}

	.container-right {

		& p {
			color: var(--bg);
		}
	}

	.timeline-container {
		display: flex;
		flex-direction: column;
		gap: 10rem;
		width: 100%;
		padding: 3vw 5vw;
		margin-top: 10rem;

		& > div {
			max-width: 38rem;
			display: flex;
			flex-direction: column;
			gap: 3.2rem;

			& span {
				color: var(--bg);
			}

			& > div {
				display: flex;
				flex-direction: column;
				gap: 1.6rem;

				& span {
					color: #ffffff9a;
				}
			}
		}
	}

	.timeline-container div:nth-child(2) {
		align-self: flex-end;
	}

	P {
		color: var(--bg);
	}

	h2 {
		color: var(--accent);
		font-size: 2rem;

		& span {
			font-size: 3rem;
		}
	}

	@media (width < 760px) {
		.container {
			grid-template-columns: 1fr;
			max-width: 100%;
			padding: 5vw;
		}

		.container span {
			width: 100%;
		}

		.container-left {
			width: 100%;
		}

		.timeline-container {
			align-items: center;
		}

		.timeline-container div:nth-child(2) {
		align-self: center;
	}

	.card {
		width: 100%;
	}
	
	}
</style>
