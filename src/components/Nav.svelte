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
				<a href="/">
					<svg id="Group_202" data-name="Group 202" xmlns="http://www.w3.org/2000/svg" width="114.077" height="45.852" viewBox="0 0 114.077 45.852">
						<path id="Path_358" data-name="Path 358" d="M414.554,416.247h4.585a4.572,4.572,0,0,0,4.522-5.234,4.671,4.671,0,0,0-4.677-3.9h-4.428a.016.016,0,0,1-.016-.016v-4.359a4.671,4.671,0,0,0-3.9-4.677,4.572,4.572,0,0,0-5.234,4.522v4.514a.016.016,0,0,1-.016.016H390.976v-4.375a4.671,4.671,0,0,0-3.9-4.677,4.572,4.572,0,0,0-5.234,4.522v4.514a.016.016,0,0,1-.016.016H377.4a4.671,4.671,0,0,0-4.677,3.9,4.571,4.571,0,0,0,4.522,5.234h4.574a.016.016,0,0,1,.016.016v13.959c0,.031,0,.06,0,.09a13.741,13.741,0,0,0,13.42,13.545,4.693,4.693,0,0,0,4.869-4.42,4.569,4.569,0,0,0-4.585-4.714,4.651,4.651,0,0,1-4.571-4.7V416.25h14.411a.016.016,0,0,1,.016.016v13.959c0,.031,0,.06,0,.09a13.741,13.741,0,0,0,13.419,13.546,4.693,4.693,0,0,0,4.869-4.421,4.569,4.569,0,0,0-4.585-4.714,4.651,4.651,0,0,1-4.571-4.7V416.268C414.539,416.253,414.546,416.247,414.554,416.247Z" transform="translate(-342.655 -398.009)" fill="#100abf"/>
						<path id="Path_359" data-name="Path 359" d="M216.715,472.21a17.765,17.765,0,0,0-16.548-17.856,17.447,17.447,0,0,0-11.455,3.408,4.683,4.683,0,0,0-1.385,6.078,4.569,4.569,0,0,0,6.721,1.34,8.35,8.35,0,0,1,5.1-1.718,8.438,8.438,0,0,1,8.082,6.053,18.042,18.042,0,0,0-7.291-2.144c-6.926-.512-13.118,4.692-13.229,11.636a11.892,11.892,0,0,0,11.878,12.073h12.536a5.589,5.589,0,0,0,5.61-5.5c0-.313-.006-.623-.021-.932Zm-18.127,9.734a2.747,2.747,0,0,1-2.691-3.274,2.832,2.832,0,0,1,2.914-2.205,9.028,9.028,0,0,1,8.068,5.48Z" transform="translate(-186.71 -445.233)" fill="#100abf"/>
						<path id="Path_360" data-name="Path 360" d="M732.775,458.928a4.569,4.569,0,0,0-4.569,4.569v12.441a5.979,5.979,0,0,1-5.192,5.995,5.882,5.882,0,0,1-6.558-5.836V459.07a4.661,4.661,0,0,0-3.891-4.663,4.571,4.571,0,0,0-5.245,4.521V475.82c0,7.749,6.308,14.768,14.043,15.257a15.028,15.028,0,0,0,15.983-14.982V463.5A4.571,4.571,0,0,0,732.775,458.928Z" transform="translate(-623.269 -445.261)" fill="#100abf"/>
					</svg>
				</a>
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
							<a href="/">
								<img class="logo" alt="attu logo" src="./images/logoNoBg.png"/>
							</a>
						</li>
					{/if}
					<li class="menu__item">
						<a href="/cinesuntem">
							<h4>Despre Noi</h4>
						</a>
					</li>
					<li class="menu__item">
						<a href="/activitati">
							<h4>Activitățile Noastre	</h4>
						</a>
					</li>
					<li class="menu__item">
						<a href="/implicate">
							<h4>Implică-te</h4>
						</a>
					</li>
					<li class="menu__item">
						<a href="/contact">
							<h4>Contact</h4>
						</a>
					</li>
				</ul>
			</li>
			
			<li class="nav__btn">
				<a href="/doneaza">
					<Button type="primary">Donează</Button> 
				</a>
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
a {
	color: #000;
  text-decoration: none;
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

