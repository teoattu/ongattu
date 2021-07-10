<script>
  import { onMount } from "svelte";
  import Button from "./Button.svelte";
  import { goto } from "@sapper/app";

  import "../css/global.css";

  let windowWidth;
  let isOpen = false;

  onMount(() => {
    if (typeof window !== undefined) {
      windowWidth = window.innerWidth;
    }
  });
</script>

<nav
  class="nav"
  on:blur={() => {
    isOpen = false;
  }}
  on:click={() => {
    isOpen = !isOpen;
  }}
>
  {#if windowWidth < 1200}
    {#if isOpen}
      <svg
        class="nav__icon"
        fill="#000"
        viewBox="0 0 20 20"
        xmlns="http://www.w3.org/2000/svg"
        ><path
          fill-rule="evenodd"
          d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
          clip-rule="evenodd"
        />
			</svg>
    {:else}
      <svg
        class="nav__icon"
        fill="#000"
        viewBox="0 0 20 20"
        xmlns="http://www.w3.org/2000/svg"
        ><path
          fill-rule="evenodd"
          d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
          clip-rule="evenodd"
        />
      </svg>
    {/if}
  {/if}
	{#if isOpen || windowWidth >= 1200}
		<div class="nav__bar">
			<a href="/"> 
        <svg xmlns="http://www.w3.org/2000/svg" width="114.078" height="45.852" viewBox="0 0 114.078 45.852">
          <g id="Logo_attu_albastru" transform="translate(0.001)">
            <path id="Path_358" data-name="Path 358" d="M414.554,416.247h4.585a4.572,4.572,0,0,0,4.522-5.234,4.671,4.671,0,0,0-4.677-3.9h-4.428a.016.016,0,0,1-.016-.016v-4.359a4.671,4.671,0,0,0-3.9-4.677,4.572,4.572,0,0,0-5.234,4.522v4.514a.016.016,0,0,1-.016.016H390.976v-4.375a4.671,4.671,0,0,0-3.9-4.677,4.572,4.572,0,0,0-5.234,4.522v4.514a.016.016,0,0,1-.016.016H377.4a4.671,4.671,0,0,0-4.677,3.9,4.571,4.571,0,0,0,4.522,5.234h4.574a.016.016,0,0,1,.016.016v13.959c0,.031,0,.06,0,.09a13.741,13.741,0,0,0,13.42,13.545,4.693,4.693,0,0,0,4.869-4.42,4.569,4.569,0,0,0-4.585-4.714,4.651,4.651,0,0,1-4.571-4.7V416.25h14.411a.016.016,0,0,1,.016.016v13.959c0,.031,0,.06,0,.09a13.741,13.741,0,0,0,13.419,13.546,4.693,4.693,0,0,0,4.869-4.421,4.569,4.569,0,0,0-4.585-4.714,4.651,4.651,0,0,1-4.571-4.7V416.268C414.539,416.253,414.546,416.247,414.554,416.247Z" transform="translate(-342.655 -398.01)" fill="#100abf"/>
            <path id="Path_359" data-name="Path 359" d="M216.715,472.21a17.765,17.765,0,0,0-16.548-17.856,17.447,17.447,0,0,0-11.455,3.408,4.683,4.683,0,0,0-1.385,6.078,4.569,4.569,0,0,0,6.721,1.34,8.35,8.35,0,0,1,5.1-1.718,8.438,8.438,0,0,1,8.082,6.053,18.042,18.042,0,0,0-7.291-2.144c-6.926-.512-13.118,4.692-13.229,11.636a11.892,11.892,0,0,0,11.878,12.073h12.536a5.589,5.589,0,0,0,5.61-5.5c0-.313-.006-.623-.021-.932Zm-18.127,9.734a2.747,2.747,0,0,1-2.691-3.274,2.832,2.832,0,0,1,2.914-2.205,9.028,9.028,0,0,1,8.068,5.48Z" transform="translate(-186.71 -445.233)" fill="#100abf"/>
            <path id="Path_360" data-name="Path 360" d="M732.775,458.928a4.569,4.569,0,0,0-4.569,4.569v12.441a5.979,5.979,0,0,1-5.192,5.995,5.882,5.882,0,0,1-6.558-5.836V459.07a4.661,4.661,0,0,0-3.891-4.663,4.571,4.571,0,0,0-5.245,4.521V475.82c0,7.749,6.308,14.768,14.043,15.257a15.028,15.028,0,0,0,15.983-14.982V463.5A4.571,4.571,0,0,0,732.775,458.928Z" transform="translate(-623.269 -445.261)" fill="#100abf"/>
          </g>
        </svg>        
			</a>
      <div class="nav__routes">
        <a href="/cinesuntem"><h4>Despre Noi</h4></a>
        <a href="/activitati"><h4>Activitătile Noastre</h4></a>
        <a href="/implicate"><h4>Implică-te!</h4></a>
        <a href="/contact"><h4>Contact</h4></a>
      </div>
      <div class="nav__button">
        <a href="/doneaza"><Button type="primary">Donează</Button></a>
        
      </div>
		</div>
	{/if}
</nav>

<style lang="scss">
  .nav {
    position: absolute;
    top: 0;
    width: 100%;
    @media (max-width:1024px) {
      background-color: #ffffff;
      position: fixed;
    }
    &__bar {
      display: flex;
      justify-content: space-between;
      padding: 50px 135px;
      
      @media (max-width:1024px) {
        flex-direction: column;
        align-items: center;
        padding: 0;
        padding-bottom: 1rem;
      } 
    }

    &__routes {
      display: flex;
      padding-left: 120px;
      a {
        margin: 0 37px;
      }
      h4 {
        font-size: 1.5rem;
      }
      @media (max-width:1024px) {
        flex-direction: column;
        align-items: center;
        width: 100%;
        padding: 0;
      }
    }
    &__icon {
      width: 50px;
      height: 50px;
      padding: 1rem;
    }
  }
</style>
