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

<section id="produits">
	<div class="container">
		<div class="header">
			<div>
				<h3>BARRIERE LEVANTE, PORTE AUTOMATIQUE, <br /> TRIPODE TOURNIQUET</h3>
			</div>
			<div>
				<p>
					Optimisez le contrôle d’accès avec no- tre service de barrières levantes et tri- podes
					automatisés. Conçus pour une gestion fluide et sécurisée des entrées, nos systèmes offrent
					une solution ro- buste et intelligente.
				</p>
			</div>
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
				Automatisez l’accès à votre domicile avec notre service de motorisation de portail innovant.
				Profitez de la com- modité de l’ouverture et de la ferme- ture automatisées, alliant
				sécurité et simplicité. Une solution intelligente pour un quotidien sans tracas.
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
			<h3>PORTE DE GARAGE</h3>
			<p>
				Transformez votre quotidien avec no- tre service de motorisation de portes de garage,
				alliant ingénierie de pointe et praticité. Ouvrez et fermez votre garage en toute
				simplicité, bénéficiant d’une sécurité renforcée.
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
		align-items: center;

		& > div {
			width: 100%;
		}
	}

	.header {
		display: grid;
		max-width: 100rem;
		grid-template-columns: repeat(auto-fill, minmax(33rem, 1fr));
		gap: 5vw;
		margin-top: 7rem;
		/* background-color: red; */
	}

	.container-products {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(30rem, 1fr));
		/* max-width: 96rem; */
		gap: 2rem;
		/* grid-template-rows: minmax(35rem, auto); */
	}

	.card img {
		/* width: 100%; */
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
		color: var(--accent);
	}

	h4 {
		font-size: 1.4rem;
		text-transform: uppercase;
		line-height: 130%;
	}

	@media (width < 700px) {
		.header {
			grid-template-columns: 1fr;
			max-width: 100%;
		}
	}

	@media (width < 400px) {
		.container-products {
			display: flex;
			flex-direction: column;
		}
	}
</style>
