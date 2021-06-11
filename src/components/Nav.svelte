<script>

	import { onMount } from 'svelte';
	import Button from './Button.svelte'
	import { goto } from '@sapper/app';

	import '../css/global.css';
	
	let windowWidth;
	let isOpen = false;

	onMount(()=> {
		if(typeof window !== undefined) {
			windowWidth = window.innerWidth;
		}
	})
	$:console.log(windowWidth)
</script>


<nav on:blur="{() => {isOpen = false}}">
	<ul>
		{#if windowWidth > 720 }
			<li class="nav__logo">
				<img class="logo" alt="attu logo" src="./images/logoNoBg.png"/>
			</li>
		{:else}
			<li class="nav__burger">
				<svg xmlns="http://www.w3.org/2000/svg" class="nav__icon" fill="none" viewBox="0 0 24 24" stroke="currentColor" on:click="{()=>{isOpen = !isOpen}}">
					<path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6h16M4 12h16M4 18h16" />
				</svg>
			</li>
		{/if}
		{#if windowWidth > 720 || isOpen}
			<li>
				<ul class="nav__routes">
					{#if windowWidth < 720 }
						<li class="nav__logo logo__small">
							<img class="logo" alt="attu logo" src="./images/logoNoBg.png"/>
						</li>
					{/if}
					<li class="menu__item">
						<a href="/cinesuntem">
							<h4>Despre Noi</h4>
						</a>
					</li>
					<li class="menu__item">
						<h4>Activitățile Noastre	</h4>
					</li>
					<li class="menu__item">
						<h4>Implică-te</h4>
					</li>
					<li class="menu__item">
						<h4>Contact</h4>
					</li>
				</ul>
			</li>
			
			<li class="nav__btn">
				<Button type="primary">Donează</Button> 
			</li>
		{/if}
	</ul>
</nav>

<style>
nav {
  position: fixed;
  top: 0;
  width: 100%;
  height: 64px;
}
nav > ul {
	margin: 0;
	padding: 0;
  display: flex;
  justify-content: space-around;
}
nav > ul > li {
  display: flex;
  justify-content: center;
  align-items: center;
	margin: 0 2rem;
}
li:first-child{
	padding: 1rem 0;
}
ul {
  list-style: none;
}
@media only screen and (max-width: 720px) {
	nav > ul > li {
		padding: 0.25rem 0;
		width: 100%;
		background-color: #ffffff8f;
	}
	.nav__routes {
		flex-direction: column;
		
	}
	.nav__routes > li {
		margin: 0;
	}
	
}	

.nav__routes { 
	display: flex;
	justify-content: center;
	align-items: center;
	padding: 0;
}
.nav__routes > li {
	margin: 0 2rem;
}

.nav__icon {
	width: 2rem;
	height: 2rem;
	align-self: flex-start;
	margin-left: 1rem;
	
}
.nav__burger {
	padding: 1rem 1rem;
	align-items: center;
	justify-content: flex-start;
}
</style>

