<script lang="ts">
	import { animate, scroll } from 'motion';
	import { onMount } from 'svelte';
	type Quality = 'performance' | 'fast' | 'robust';

	let qualityState: Quality = 'performance';

	onMount(() => {
		scroll(animate('.progress', { strokeDasharray: ['0,1', '1,1'] }), {
			target: document.querySelector('.right') as HTMLDivElement
		});

		const rightEls = [...document.querySelectorAll('.right > div')];

		let callback: IntersectionObserverCallback = (entries) => {
			const currentEl = entries[0].target as HTMLDivElement;
			qualityState = currentEl.dataset.state as Quality;
		};
		let option: IntersectionObserverInit = {
			// root: document.querySelector('.right'),
			threshold: 0.85
		};

		let observer = new IntersectionObserver(callback, option);

		rightEls.forEach((item) => {
			observer.observe(item);
		});
	});
</script>

<section>
	<div class="left">
		<div class="container">
			<svg viewBox="0 0 100 100">
				<circle cx="50" cy="50" r="45" pathLength="1" class="bg" />
				<circle cx="50" cy="50" r="45" pathLength="1" class="progress" />
			</svg>
			<div class="picto">
				{#if qualityState === 'performance'}
					<img src="/perf.svg" alt="pictogramme" />
				{/if}
				{#if qualityState === 'fast'}
					<img src="/fast.svg" alt="pictogramme" />
				{/if}
				{#if qualityState === 'robust'}
					<img src="/robust.svg" alt="pictogramme" />
				{/if}
			</div>
		</div>
	</div>
	<div class="right">
		<div data-state="performance">
			<div class="header">
				<h3>SECURITY</h3>
				<span />
			</div>
			<div>
				<p>
					Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore sunt dolorum fugiat,
					voluptates totam, nulla, eveniet quos nisi officia ducimus est libero quam iusto
					reiciendis illum tempora. Ab, omnis corrupti!
				</p>
			</div>
		</div>

		<!-- 1 -->
		<div data-state="fast">
			<div class="header">
				<h3>SECURITY</h3>
				<span />
			</div>
			<div>
				<p>
					Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore sunt dolorum fugiat,
					voluptates totam, nulla, eveniet quos nisi officia ducimus est libero quam iusto
					reiciendis illum tempora. Ab, omnis corrupti!
				</p>
			</div>
		</div>
		<div data-state="robust">
			<div class="header">
				<h3>SECURITY</h3>
				<span />
			</div>
			<div>
				<p>
					Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore sunt dolorum fugiat,
					voluptates totam, nulla, eveniet quos nisi officia ducimus est libero quam iusto
					reiciendis illum tempora. Ab, omnis corrupti!
				</p>
			</div>
		</div>
	</div>
</section>

<style>
	section {
		width: 100%;
		height: 250dvh;
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		/* background-color: var(--secondary); */
	}

	.left {
		position: sticky;
		top: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100dvh;
		/* background-color: var(--accent); */
	}

	.container {
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		/* left: 50%; */
		/* background-color: rebeccapurple; */
		width: 35rem;
		height: 35rem;
	}

	.right {
		padding: 5vw;
		background-color: var(--secondary);
		color: var(--bg);
	}

	.right > div {
		height: 80dvh;
		display: flex;
		flex-direction: column;
		gap: 20px;
		display: flex;
		flex-direction: column;
		align-items: center;

		& h3 {
			font-size: clamp(20px, 2vw + 0.1rem, 3rem);
		}

		& p {
			color: var(--bg);
		}
	}

	.right div:nth-child(3) {
		height: 40dvh;
		/* background-color: rebeccapurple; */
	}

	.header {
		display: flex;
		width: 100%;
		gap: 20px;
		align-items: center;

		& span {
			height: 2px;
			width: 70%;
			background-color: var(--accent);
			flex-shrink: 2;
		}
	}

	svg {
		transform: rotate(-90deg);
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		/* background-color: red; */
		width: 90%;
		height: 90%;
	}

	circle {
		stroke-dashoffset: 0;
		stroke-width: 5%;
		fill: none;
	}

	.bg {
		stroke: var(--secondary);
	}

	.progress {
		stroke: var(--accent);
		stroke-dasharray: 0, 1;
	}

	img {
		height: 100%;
		width: 100%;
		object-fit: contain;
	}

	.picto {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		/* background-color: aquamarine; */
		z-index: 3;
		width: 10rem;
		height: 10rem;
	}
</style>
