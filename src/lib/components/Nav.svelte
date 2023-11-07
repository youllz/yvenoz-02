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
<div class="nav-container" transition:fly={{y: '-500', duration: 1000, easing: quadInOut}}>
	<ul class="menu">
		{#each url as item}
			<li>
				<a href={item.url}>{item.title}</a>
				<span></span>
			</li>
		{/each}
	</ul>
	<div class="container-bottom">
		<ul class="social">
			<li>
				<a  href="mailto:yvenoz.services@outlook.fr" target="_blank">
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M4 20q-.825 0-1.413-.588T2 18V6q0-.825.588-1.413T4 4h16q.825 0 1.413.588T22 6v12q0 .825-.588 1.413T20 20H4Zm8-7l8-5V6l-8 5l-8-5v2l8 5Z"/></svg>
					</span>
				</a>
			</li>
			<li>
				<a href="https://wa.me/33623381963" target="_blank">
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M12.001 2c5.523 0 10 4.477 10 10s-4.477 10-10 10a9.954 9.954 0 0 1-5.03-1.355L2.005 22l1.352-4.968A9.953 9.953 0 0 1 2.001 12c0-5.523 4.477-10 10-10ZM8.593 7.3l-.2.008a.961.961 0 0 0-.372.1a1.293 1.293 0 0 0-.294.228c-.12.113-.188.211-.261.306A2.73 2.73 0 0 0 6.9 9.62c.002.49.13.967.33 1.413c.409.902 1.082 1.857 1.97 2.742c.214.213.424.427.65.626a9.448 9.448 0 0 0 3.84 2.046l.568.087c.185.01.37-.004.556-.013a1.99 1.99 0 0 0 .833-.231a4.83 4.83 0 0 0 .383-.22s.043-.028.125-.09c.135-.1.218-.171.33-.288c.083-.086.155-.187.21-.302c.078-.163.156-.474.188-.733c.024-.198.017-.306.014-.373c-.004-.107-.093-.218-.19-.265l-.582-.261s-.87-.379-1.402-.621a.497.497 0 0 0-.176-.041a.482.482 0 0 0-.378.127c-.005-.002-.072.055-.795.931a.35.35 0 0 1-.368.13a1.43 1.43 0 0 1-.191-.066c-.124-.052-.167-.072-.252-.108a6.025 6.025 0 0 1-1.575-1.003c-.126-.11-.243-.23-.363-.346a6.297 6.297 0 0 1-1.02-1.268l-.059-.095a.923.923 0 0 1-.102-.205c-.038-.147.061-.265.061-.265s.243-.266.356-.41c.11-.14.203-.276.263-.373c.118-.19.155-.385.093-.536c-.28-.684-.57-1.365-.868-2.041c-.059-.134-.234-.23-.393-.249c-.054-.006-.108-.012-.162-.016a3.385 3.385 0 0 0-.403.004l.201-.008Z"/></svg>
					</span>
				</a>
			</li>
			<li>
				<a href="https://www.facebook.com/profile.php?id=100064108421949" target="_blank">
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 4.84 3.44 8.87 8 9.8V15H8v-3h2V9.5C10 7.57 11.57 6 13.5 6H16v3h-2c-.55 0-1 .45-1 1v2h3v3h-3v6.95c5.05-.5 9-4.76 9-9.95z"/></svg>
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
{/if}


<style>
	.nav-container {
		width: 100%;
		position: fixed;
		top: 0;
		background-color: var(--secondary);
		color: var(--bg);
		min-height: 80vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 10vw 5vw 5vw;
		z-index: 40;
		gap: 10rem;
	}

	.menu {
		width: 70vw;
		display: flex;
		flex-direction: column;
		min-height: 10rem;

		& li {
			flex: 1;
			/* border-bottom: 1px solid white; */
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			width: 100%;
			position: relative;
			overflow: hidden;
		}


		& a {
			font-size: 5vw;
			user-select: none;
			transition: all 0.3s ease-out;
		}

		& a:hover {
			padding-left: 20px;
		}
		
	}


	.container-bottom {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 5rem;
		flex-wrap: wrap;


		& ul {
			display: flex;
			align-items: center;
			gap: 2rem;

		}
	}

	.phone span {
		font-size: clamp(14px, 2vw + 0.1rem, 1.6rem );
	}

	.menu span {
		display: inline-block;
		position: absolute;
		bottom: 0;
		height: 1px;
		width: 100%;
		background-color: var(--bg);
	}

	@media (width < 627px) {
		.container-bottom {
			justify-content: center;
			align-items: center;
		}
	}
</style>