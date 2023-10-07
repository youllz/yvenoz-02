<section id="contacts">
	<div class="container">
		<div class="container-left">
			<span />
			<h3>Contacts</h3>
		</div>
		<div class="container-right">
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore eius sed dicta, beatae porro
				laboriosam pariatur voluptatum animi autem expedita! Quos voluptate aliquid vel at quae rem
				numquam explicabo exercitationem.
			</p>
		</div>
	</div>

	<div class="contacts-container">
		<ul class="social">
			<li>
				<a href="mailto:yvenoz.services@outlook.fr" target="_blank"> Mail </a>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
						><path
							fill="none"
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M12 6H6a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2v-6m-7 1l9-9m-5 0h5v5"
						/></svg
					>
				</span>
			</li>
			<li>
				<a href="https://wa.me/33623381963" target="_blank"> Whatsapp </a>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
						><path
							fill="none"
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M12 6H6a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2v-6m-7 1l9-9m-5 0h5v5"
						/></svg
					>
				</span>
			</li>
			<li>
				<a href="https://www.facebook.com/profile.php?id=100064108421949" target="_blank">
					facebook
				</a>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
						><path
							fill="none"
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M12 6H6a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2v-6m-7 1l9-9m-5 0h5v5"
						/></svg
					>
				</span>
			</li>
		</ul>
	</div>
</section>

<style>
	section {
		width: 100%;
		min-height: 100dvh;
		padding: 5vw;
		background-color: var(--secondary);
		display: flex;
		flex-direction: column;
		align-items: center;
		padding-top: 20vw;
		gap: 10vw;
	}

	.container {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		max-width: 70%;
	}

	.container-left {
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

	.container-right {
		display: flex;
		flex-direction: column;
		gap: 16px;

		& p {
			color: var(--bg);
		}
	}

	.contacts-container {
		width: 100%;
		margin-top: 6rem;
		display: flex;
		align-items: center;
		justify-items: center;
		/* background-color: red; */
	}

	.contacts-container ul {
		display: flex;
		flex-direction: column;
		gap: 2rem;
	}

	li {
		position: relative;
		display: flex;
		align-items: center;
		gap: 1rem;

		& a {
			width: 100%;
			height: 100%;
			color: var(--bg);
			font-size: clamp(18px, 2vw + 0.1rem, 2.5rem);
			font-family: var(--headline);
		}

		& span {
			color: var(--accent);
		}
	}

	.social li::before {
		position: absolute;
		bottom: 0;
		transition: tranform 0.3s ease-out;
		transform-origin: left;
		display: inline-block;
		width: 100%;
		height: 3px;
		background-color: var(--accent);
	}
</style>
