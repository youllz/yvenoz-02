<script lang="ts">
	let cardsData = {
		motor: [
			{
				img: '/motorisation-portail/product1.webp',
				title: 'Kit de motorisation portail battant'
			},
			{
				img: '/motorisation-portail/product2.webp',
				title: 'Kit de motorisation portail battant'
			},
			{
				img: '/motorisation-portail/product3.webp',
				title: 'Kit de motorisation portail coulissant'
			}
		],

		barriere: [
			{
				img: '/barriere/product1.webp',
				title: 'Barrière automatique '
			},
			{
				img: '/barriere/product2.webp',
				title: 'Kit de barrière à chaine'
			},
			{
				img: '/barriere/product3.webp',
				title: 'Tambour de sécurité pour accès piéton'
			},
			// {
			//   img: "/barriere/product4.webp",
			//   title: "Portillon tripode",
			// },
			{
				img: '/barriere/product4.webp',
				title: 'Porte automatique'
			}
		],

		porteGarage: [
			// {
			//   img: "/porte-garage/product1.webp",
			//   title: "",
			// },
			{
				img: '/porte-garage/product2.webp',
				title: 'Kits complets pour de garage'
			},
			{
				img: '/porte-garage/product3.webp',
				title: 'Moteur pour porte de garage'
			}
			// {
			// 	img: '/porte-garage/product4.webp',
			// 	title: ''
			// },
			// {
			// 	img: '/porte-garage/product5.jpg',
			// 	title: ''
			// }
		]
	};
</script>

<section>
	<div>
		<h2>Nos produits</h2>
	</div>

	<div class="container">
		<div class="header">
			<h3>BARRIERE LEVANTE, PORTE AUTOMATIQUE, <br /> TRIPODE TOURNIQUET</h3>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam eligendi error nemo
				perferendis sequi itaque debitis illo, magni sunt et rerum, voluptatum eum asperiores
				nostrum eaque temporibus saepe, non natus!
			</p>
		</div>

		<div class="container-products">
			{#each cardsData.barriere as item}
				<div class="card">
					<img src="/products{item.img}" alt={item.title} />
					<h4>
						{item.title}
					</h4>
				</div>
			{/each}
		</div>
	</div>

	<!--  -->

	<div class="container">
		<div class="header">
			<h3>MOTORISATION PORTAIL</h3>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam eligendi error nemo
				perferendis sequi itaque debitis illo, magni sunt et rerum, voluptatum eum asperiores
				nostrum eaque temporibus saepe, non natus!
			</p>
		</div>

		<div class="container-products">
			{#each cardsData.motor as item}
				<div class="card">
					<img src="/products{item.img}" alt={item.title} />
					<h4>
						{item.title}
					</h4>
				</div>
			{/each}
		</div>
	</div>

	<!--  -->
	<div class="container">
		<div class="header">
			<h3>BARRIERE LEVANTE PORTE AUTOMATIQUE TRIPODE TOURNIQUET</h3>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam eligendi error nemo
				perferendis sequi itaque debitis illo, magni sunt et rerum, voluptatum eum asperiores
				nostrum eaque temporibus saepe, non natus!
			</p>
		</div>

		<div class="container-products">
			{#each cardsData.porteGarage as item}
				<div class="card">
					<img src="/products{item.img}" alt={item.title} />
					<h4>
						{item.title}
					</h4>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		width: 100%;
		min-height: 100dvh;
		background-color: var(--bg);
		padding: 2vw 5vw 5vw;
	}

	.container {
		width: 100%;
		display: flex;
		flex-direction: column;
		gap: 10rem;
		margin-top: 15rem;

		& > div {
			width: 100%;
		}
	}

	.header {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		margin-top: 7rem;
	}

	.container-products {
		display: grid;
		grid-template-columns: repeat(auto-fill, 30rem);
		/* grid-template-rows: minmax(35rem, auto); */
	}

	.card img {
		width: 100%;
		height: 20rem;
		object-fit: contain;
	}

	.card {
		text-align: center;
		/* align-items: center; */
		display: flex;
		flex-direction: column;
		gap: 2rem;
		/* background-color: red; */
	}

	h3 {
		font-size: 2rem;
		line-height: 100%;
	}

	h4 {
		font-size: 1.4rem;
	}
</style>
