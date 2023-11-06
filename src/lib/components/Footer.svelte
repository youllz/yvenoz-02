<script lang="ts">
	const url = [
		{
			url: '/#acceuil',
			title: 'ACCEUIL'
		},
		{
			url: '/#services',
			title: 'SERVICES'
		},
		{
			url: '/#contacts',
			title: 'CONTACTS'
		}
	];
</script>

<section>
	<div class="top">
		<ul>
			<li>
				<a href="/">
					<span class="logo"> Yvenoz Services </span>
				</a>
			</li>
			<li>
				<a href="#accueil">
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
							><path
								fill="currentColor"
								d="m4 12l1.41 1.41L11 7.83V20h2V7.83l5.58 5.59L20 12l-8-8l-8 8z"
							/></svg
						>
					</span>
				</a>
			</li>
		</ul>
	</div>
	<div class="middle">
		<ul class="social">
			<li>
				<a href="https://www.facebook.com/profile.php?id=100064108421949" target="_blank">
					<span>Facebook</span>
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24"
							><path fill="currentColor" d="M6 6v2h8.59L5 17.59L6.41 19L16 9.41V18h2V6z" /></svg
						>
					</span>
				</a>
			</li>
			<li>
				<a href="mailto:yvenoz.services@outlook.fr" target="_blank">
					<span>Mail</span>
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24"
							><path fill="currentColor" d="M6 6v2h8.59L5 17.59L6.41 19L16 9.41V18h2V6z" /></svg
						>
					</span>
				</a>
			</li>
			<li>
				<a href="https://wa.me/33623381963" target="_blank">
					<span>Whatsapp</span>
					<span>
						<span>
							<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24"
								><path fill="currentColor" d="M6 6v2h8.59L5 17.59L6.41 19L16 9.41V18h2V6z" /></svg
							>
						</span>
					</span>
				</a>
			</li>
		</ul>

		<ul class="phone">
			<li><span>+225 07 24 32 09</span></li>
			<li><span>+225 01 03 69 60 09</span></li>
			<li><span>33(0) 623 28 19 63</span></li>
		</ul>

		<ul class="menu">
			{#each url as item}
				<li>
					<a href={item.url}>
						<span>{item.title}</span>
					</a>
				</li>
			{/each}
		</ul>
	</div>
	<div class="bottom" />
</section>

<style>
	section {
		width: 100%;
		min-height: 30dvh;
		background-color: var(--secondary);
	}

	.top {
		width: 100%;
		border-bottom: 0.1px solid #ffffff41;

		& ul {
			display: flex;
			align-items: center;
			justify-content: space-between;
			padding: 3vw 5vw;
			color: var(--bg);
		}
	}

	.logo {
		font-family: var(--headline);
		font-size: 3dvw;
	}

	.middle {
		width: 100%;
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(40rem, 1fr));
		gap: 2rem;
		place-items: center;
		color: var(--bg);
		padding: 2vw 0;

		& ul {
			display: flex;
			align-items: center;
			gap: 2rem;
		}
	}

	.phone {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.phone span,
	a {
		font-size: clamp(14px, 1.5vw + 0.1rem, 1.8rem);
		text-transform: uppercase;
	}


	@media (width < 415px) {
		.middle {
			grid-template-columns: 1fr;
			padding: 20px 10px;
			
		}

		.phone {
			flex-wrap: wrap;
			justify-content: center;
		}

		.phone span,
	a {
		font-size: 10px;
		text-transform: uppercase;

	}

	}
</style>
