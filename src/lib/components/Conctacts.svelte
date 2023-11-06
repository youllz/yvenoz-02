<section class="container" id="contacts">
	<div class="left">
		<figure>
			<img src="/contact.webp" alt="contact" />
		</figure>
	</div>
	<div class="right">
		<div class="header">
			<div class="header-left">
				<span />
				<h3>CONTACTS</h3>
			</div>
			<div class="header-right">
				<p>
					Si vous avez besoin d'une assistance immédiate, notre numéro de téléphone est à votre
					disposition. Nous comprenons que certaines questions ou préoccupations nécessitent une
					réponse rapide
				</p>
			</div>
		</div>

		<div class="body">
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
		</div>
	</div>
</section>

<style>
	section {
		max-height: 110dvh;
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: minmax(20rem, auto);
		place-content: center;
		padding: 5vw;
		gap: 3rem;
	}

	.header {
		display: grid;
		grid-template-columns: repeat(1, 1fr);
		max-width: 80%;
		gap: 2rem;
	}

	.header-left {
		& span {
			display: inline-block;
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

	.header-right {
		display: flex;
		flex-direction: column;
		gap: 16px;
		& h2 {
			font-size: clamp(3rem, 2vw + 0.1rem, 4rem);
			line-height: 90%;
			text-transform: uppercase;
		}
	}

	figure {
		height: 50%;
	}

	.left figure,
	img {
		width: 100%;
		height: 100%;
		object-position: top;
	}

	img {
		object-fit: cover;
	}

	.body {
		width: 100%;
		display: flex;
		flex-direction: column;
		gap: 6vw;
		margin-top: 8rem;
	}

	.right {
		justify-content: center;
		display: flex;
		flex-direction: column;
	}

	.social {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
	}

	.phone {
		display: flex;
		gap: 0.5rem;
		justify-content: space-between;

		& span {
			font-size: clamp(14px, 1vw + 0.1rem, 1.8rem);
		}
	}

	.social li {
		position: relative;
		overflow: hidden;
		display: flex;
		align-items: center;
	}

	.social a {
		width: 100%;
		transition: all 0.3s ease-out;
		text-transform: uppercase;
	}

	.social li:hover a {
		padding-left: 10px;
	}

	.social li:nth-child(2) a {
		align-self: flex-end;
		/* color: red; */
	}

	.social li::before {
		content: '';
		position: absolute;
		height: 2px;
		width: 100%;
		display: inline-block;
		background-color: var(--accent);
		bottom: -1px;
	}

	@media (width < 860px ) {
		section {
			grid-template-columns: 1fr;
		}
	}

	@media (width < 450px) {
		.phone {
			flex-wrap: wrap;
			gap: 20px;
		}

		.header {
			max-width: 100%;

		}
			.header span {
				width: 100%;
			}
	}
</style>
