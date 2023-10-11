<script lang="ts">
	import {
		quadInOut,
		quadOut,
		quartOut,
		expoInOut,
		cubicOut,
		cubicIn,
		linear
	} from 'svelte/easing';
	import { fade, fly, slide } from 'svelte/transition';

	export let navIsOpen: boolean;

	const url = [
		{
			url: '#accueil',
			title: 'ACCUEIL'
		},
		{
			url: '#services',
			title: 'SERVICES'
		},
		{
			url: '#contacts',
			title: 'CONTACTS'
		}
	];
</script>

{#if navIsOpen}
	<div class="container" transition:slide={{ axis: 'x', duration: 1000, easing: linear }}>
		<div class="container__right">
			<ul class="menu">
				{#each url as item}
					<li>
						<a href={item.url}>
							<span>{item.title}</span>
						</a>
					</li>
				{/each}
			</ul>

			<div class="container__right-bottom">
				<ul>
					<li>
						<a href="https://www.facebook.com/profile.php?id=100064108421949" target="_blank">
							<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
								><path
									fill="currentColor"
									d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 4.84 3.44 8.87 8 9.8V15H8v-3h2V9.5C10 7.57 11.57 6 13.5 6H16v3h-2c-.55 0-1 .45-1 1v2h3v3h-3v6.95c5.05-.5 9-4.76 9-9.95z"
								/></svg
							>
						</a>
					</li>
					<li>
						<a href="mailto:yvenoz.services@outlook.fr" target="_blank">
							<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
								><path
									fill="currentColor"
									d="M19 22q-1.65 0-2.825-1.175T15 18v-4.5q0-1.05.725-1.775T17.5 11q1.05 0 1.775.725T20 13.5V18h-2v-4.5q0-.2-.15-.35T17.5 13q-.2 0-.35.15t-.15.35V18q0 .825.588 1.413T19 20q.825 0 1.413-.588T21 18v-4h2v4q0 1.65-1.175 2.825T19 22ZM3 18q-.825 0-1.413-.588T1 16V4q0-.825.588-1.413T3 2h16q.825 0 1.413.588T21 4v6h-3.5q-1.45 0-2.475 1.025T14 13.5V18H3Zm8-7l8-5V4l-8 5l-8-5v2l8 5Z"
								/></svg
							>
						</a>
					</li>
					<li>
						<a href="https://wa.me/33623381963" target="_blank">
							<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
								><path
									fill="currentColor"
									d="M12.001 2c5.523 0 10 4.477 10 10s-4.477 10-10 10a9.954 9.954 0 0 1-5.03-1.355L2.005 22l1.352-4.968A9.953 9.953 0 0 1 2.001 12c0-5.523 4.477-10 10-10ZM8.593 7.3l-.2.008a.961.961 0 0 0-.372.1a1.293 1.293 0 0 0-.294.228c-.12.113-.188.211-.261.306A2.73 2.73 0 0 0 6.9 9.62c.002.49.13.967.33 1.413c.409.902 1.082 1.857 1.97 2.742c.214.213.424.427.65.626a9.448 9.448 0 0 0 3.84 2.046l.568.087c.185.01.37-.004.556-.013a1.99 1.99 0 0 0 .833-.231a4.83 4.83 0 0 0 .383-.22s.043-.028.125-.09c.135-.1.218-.171.33-.288c.083-.086.155-.187.21-.302c.078-.163.156-.474.188-.733c.024-.198.017-.306.014-.373c-.004-.107-.093-.218-.19-.265l-.582-.261s-.87-.379-1.402-.621a.497.497 0 0 0-.176-.041a.482.482 0 0 0-.378.127c-.005-.002-.072.055-.795.931a.35.35 0 0 1-.368.13a1.43 1.43 0 0 1-.191-.066c-.124-.052-.167-.072-.252-.108a6.025 6.025 0 0 1-1.575-1.003c-.126-.11-.243-.23-.363-.346a6.297 6.297 0 0 1-1.02-1.268l-.059-.095a.923.923 0 0 1-.102-.205c-.038-.147.061-.265.061-.265s.243-.266.356-.41c.11-.14.203-.276.263-.373c.118-.19.155-.385.093-.536c-.28-.684-.57-1.365-.868-2.041c-.059-.134-.234-.23-.393-.249c-.054-.006-.108-.012-.162-.016a3.385 3.385 0 0 0-.403.004l.201-.008Z"
								/></svg
							>
						</a>
					</li>
				</ul>
				<ul>
					<li><span>+225 07 24 32 09</span></li>
					<li><span>+225 01 03 69 60 09</span></li>

					<li><span>33(0) 623 28 19 63</span></li>
				</ul>
			</div>
		</div>

		<!-- {#if navIsOpen}
			<div
				class="container__left"
				transition:slide={{ axis: 'x', duration: 1200, easing: quartOut, delay: 500 }}
			>
				sxzczxcd
			</div>
		{/if} -->
	</div>
{/if}

<style>
	.container {
		width: 100dvw;
		/* background-color: #000000; */
		color: #f2f2f2;
		height: 100dvh;
		/* padding: 10vw 3vw; */
		position: fixed;
		top: 0;
		z-index: 40;
		right: 0;
	}

	.container__right {
		display: flex;
		justify-content: space-between;
		flex-direction: column;
		& .menu {
			width: 100%;
			display: flex;
			flex-direction: column;
			height: 60%;
			gap: 1rem;

			& li {
				flex: 1;
				position: relative;
			}

			& a {
				font-size: clamp(18px, 2vw, 3rem);
				height: 100%;
				padding-left: 2rem;
				width: 100%;
				display: flex;
				align-items: center;
				position: relative;
				color: var(--bg);
				transition: padding-left 0.2s ease-out;
			}

			& a:hover {
				padding-left: 4rem;
			}

			& li::before {
				content: '';
				position: absolute;
				display: inline-block;
				height: 2px;
				width: 100%;
				background-color: #f2f2f2;
				bottom: 0;
			}
		}
	}

	.container > div {
		height: 100%;
		/* background-color: var(--on-bg); */
		color: var(--on-bg);
		padding: 10vw 3vw 2vw;
	}

	.container__right {
		width: 50%;
		position: absolute;
		z-index: 40;
		bottom: 0;
		background-color: var(--on-bg);
		background-color: var(--secondary);
		right: 0;
	}

	.container__right-bottom {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		position: relative;

		& ul {
			display: flex;
			align-items: center;
			gap: 2rem;
			color: var(--bg);
			flex-shrink: 0;
		}

		& span {
			font-size: 1.4rem;
			font-family: var(--headline);
		}
	}
</style>
