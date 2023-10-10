<section class="container">
	<div class="left">
		<figure>
			<img src="/contact.webp" alt="contact" />
		</figure>
	</div>
	<div class="right">
		<div class="header">
			<div class="header-left">
				<span />
				<h3>Contacts</h3>
			</div>
			<div class="header-right">
				<p>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore eius sed dicta, beatae
					porro laboriosam pariatur voluptatum animi autem expedita! Quos voluptate aliquid vel at
					quae rem numquam explicabo exercitationem.
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
		height: 100dvh;
		width: 100%;
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(50rem, 1fr));
		grid-template-rows: minmax(30rem, auto);
		place-content: center;
		padding: 5vw;
		gap: 3vw;
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

	.left figure,
	img {
		width: 100%;
		height: 100%;
	}

	img {
		object-fit: cover;
	}

	.body {
		width: 100%;
		display: flex;
		flex-direction: column;
		gap: 4vw;
		margin-top: 8rem;
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
</style>
