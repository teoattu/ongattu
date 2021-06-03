<script>

	import { onMount } from 'svelte';
	import Button from './Button.svelte'

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


<nav>
	<ul>
		<li on:click="{()=>{isOpen = !isOpen}}">
			<img class="logo" alt="attu logo" src="./images/logoNoBg.png"/>
		</li>
		{#if windowWidth > 720 || isOpen}
			<li class="menu__item">
				<h4>Despre Noi</h4>
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
			<li>
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
}
</style>

