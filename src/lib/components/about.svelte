<section>
	<div class="container">
		<div class="container-left">
			<span />
			<h3>A propos</h3>
		</div>
		<div class="container-right">
			<h2>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis</h2>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore eius sed dicta, beatae porro
				laboriosam pariatur voluptatum animi autem expedita! Quos voluptate aliquid vel at quae rem
				numquam explicabo exercitationem.
			</p>
		</div>
	</div>
</section>

<style>
	section {
		width: 100%;
		height: 80dvh;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.container {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(40rem, 1fr));
		/* place-items: center; */
		gap: 3rem;
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
		& h2 {
			font-size: clamp(3rem, 2vw + 0.1rem, 4rem);
			line-height: 90%;
			text-transform: uppercase;
		}
	}
</style>
