<script>
	const logoData = [
		{
			name: 'Came Nice',
			img: '/logos/came-nice.svg'
		},
		{
			name: 'Ditec',
			img: '/logos/ditec-logo.svg'
		},
		{
			name: 'FAAC',
			img: '/logos/faac.webp'
		},
		{
			name: 'KONE',
			img: '/logos/KONE_logo.svg'
		},
		{
			name: 'Lift Master',
			img: '/logos/lift-master.webp'
		},
		{
			name: 'Somfy',
			img: 'logos/logo_somfy_2.webp'
		},
		{
			name: 'BFT',
			img: 'logos/logo-big-bft.svg'
		},
		{
			name: 'Portalp',
			img: 'logos/logo-portalp.webp'
		}
	];
	
</script>

<section>
	<div class="container">
		<div class="left">
			<span />
			<h3>pourquoi nous ?</h3>
		</div>
		<div class="right">
			<div class="para">
				<p>
					YVENOZ et ses marques partenaires certifie CE, vous garantissiez du matériel de qualité et
					faites de la satisfaction client notre priorité
				</p>
			</div>
			<div class="logo-container">
					{#each logoData as data}
						<figure>
							<img src={data.img} alt={data.name} />
						</figure>
					{/each}
			</div>
		</div>
	</div>

</section>

<style>
	section {
		width: 100%;
		min-height: 60dvh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 12rem;
	}

	.logo-container {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(7rem, 1fr));
		gap: 3vw;
		/* grid-template-rows: minmax(3rem, 1fr); */

	}

	.right {
		/* background-color: red; */
		display: flex;
		flex-direction: column;
		gap: 5vw;
	}

	
	figure {
		width: 7rem;
		height: 7rem;
		flex: 0 0 auto;
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: contain;
		filter: grayscale(10);
	}

	.container {
		display: grid;
		max-width: 100rem;
		place-content: center;
		grid-template-columns: repeat(auto-fill, minmax(33rem, 1fr));
		gap: 3rem;
		margin-top: 10rem;
	}

	.container div:nth-child(1) {
		display: flex;
		flex-direction: column;

		& span {
			width: 70%;
			height: 2px;
			background-color: var(--accent);
		}

		& h3 {
			margin-top: 0.5rem;
			color: var(--accent);
			font-size: 1.4rem;
			text-transform: uppercase;
		}
	}

	@media (width < 800px) {
		figure {
			width: 50px;
			height: 50px;
		}
	}

	@media (width < 750px) {
		.container {
			grid-template-columns: 1fr;
			max-width: none;
			padding: 0 5vw;
		}

		.container div:nth-child(1) span {
			width: 100%;
		}

		section {
			height: 70dvh;
		}
	}
</style>
