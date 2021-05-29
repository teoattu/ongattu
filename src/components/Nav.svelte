<script>

	import { onMount } from 'svelte';

	import '../css/global.css';
	
	let windowWidth;
	let isOpen = false;

	onMount(()=> {
		if(typeof window !== undefined) {
			windowWidth =  window.innerWidth;
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
			<button class="btn__primary">Donează</button>
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
  padding-top: 1rem;
  display: flex;
  justify-content: space-around;
}
nav > ul > li {
  display: flex;
  justify-content: center;
  align-items: center;
}
ul {
  list-style: none;
}
</style>

