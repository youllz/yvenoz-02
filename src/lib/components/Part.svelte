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
		}
	];
	const logoData1 = [
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
	<div class="title">
		<div>
			<span />
			<h3>partenaires</h3>
		</div>
		<div>
			<p>
				YVENOZ et ses marques partenaires certifie CE, vous garantissent du materiel de qualite et
				faisons de la satisfaction client notre priorite
			</p>
		</div>
	</div>

	<div class="logo-container">
		<div class="logo1">
			{#each logoData as data}
				<figure>
					<img src={data.img} alt={data.name} />
				</figure>
			{/each}
		</div>
		<div class="logo2">
			{#each logoData1 as data}
				<figure>
					<img src={data.img} alt={data.name} />
				</figure>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		width: 100%;
		height: 100dvh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 12rem;
	}

	.logo-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 16px;
	}

	.logo-container > div {
		display: flex;
		align-items: center;
		gap: 7vw;
	}

	figure {
		width: 100px;
		height: 100px;
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: contain;
		/* filter: grayscale(10); */
	}

	.title {
		max-width: 80%;
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		max-width: 70%;
	}

	.title div:nth-child(1) {
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
		}
	}

	p {
		font-size: 2rem;
	}
</style>
