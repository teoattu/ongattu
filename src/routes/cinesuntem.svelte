<script>
  import RoundImage from "../components/RoundImage.svelte";
  import "../css/global.css";
  import { onMount } from "svelte";

  let windowWidth;
  onMount(() => {
    if (typeof window !== undefined) {
      windowWidth = window.innerWidth;
    }
  });
</script>

<svelte:head>
  <title>Cine Suntem</title>
</svelte:head>

<div class="wrapper">
  <section class="cinesuntem__main">
    <div class="cinesuntem__main__text">
      <div>
        <h2>CINE SUNTEM</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
      </div>
    </div>
      <div class="cinesuntem__main__img">
        <RoundImage src={"/images/cinesuntem/cinesuntem.jpg"} width={windowWidth < 720 ? 320 : 640} height={windowWidth < 720 ? 320 : 640}/>
      </div>
  </section>
  <section class="cinesuntem__second">
    <h3>Viziune</h3>
    <p style="text-align: center;">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur.
    </p>
    <div style="display: flex; justify-content: center;padding:1rem">
      <svg height="64" width="1">
        <line x1="0" y1="0" x2="0" y2="200" style="stroke:rgb(0,0,0);stroke-width:2" />
        Sorry, your browser does not support inline SVG.
      </svg>
    </div>
    <h3>Misiune</h3>
    <p style="text-align: center;">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation 
    </p>
    <div style="display: flex; justify-content: center;padding:1rem">
      <svg height="64" width="1">
        <line x1="0" y1="0" x2="0" y2="200" style="stroke:rgb(0,0,0);stroke-width:2" />
        Sorry, your browser does not support inline SVG.
      </svg>
    </div>
    <h3>Valori</h3>
    <div class="cinesuntem__valori">
      <div class="cinesuntem__valori__text">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <circle id="Ellipse_340" data-name="Ellipse 340" cx="12" cy="12" r="12" fill="#100abf"/>
        </svg>
        <h3 style="padding:0.5rem">Solidaritate</h3>
      </div>
      <div class="cinesuntem__valori__text">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <circle id="Ellipse_340" data-name="Ellipse 340" cx="12" cy="12" r="12" fill="#100abf"/>
        </svg>
        <h3 style="padding:0.5rem">Umanitate</h3>
      </div>
      <div class="cinesuntem__valori__text">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <circle id="Ellipse_340" data-name="Ellipse 340" cx="12" cy="12" r="12" fill="#100abf"/>
        </svg>
        <h3 style="padding:0.5rem">Integritate</h3>
      </div>
      <div class="cinesuntem__valori__text">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <circle id="Ellipse_340" data-name="Ellipse 340" cx="12" cy="12" r="12" fill="#100abf"/>
        </svg>
        <h3 style="padding:0.5rem">Egalitate</h3>
      </div>
      <div class="cinesuntem__valori__text">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <circle id="Ellipse_340" data-name="Ellipse 340" cx="12" cy="12" r="12" fill="#100abf"/>
        </svg>
        <h3 style="padding:0.5rem">Incluziune</h3>
      </div>
      <div class="cinesuntem__valori__text">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
          <circle id="Ellipse_340" data-name="Ellipse 340" cx="12" cy="12" r="12" fill="#100abf"/>
        </svg>
        <h3 style="padding:0.5rem">Implicare</h3>
      </div>
  
    </div>


  </section>
</div>

<style>
  .wrapper {
    width: 100%;
  }
  .cinesuntem__main {
    height: 100vh;
    padding-top: 64px;
    padding-left: 2rem;
    padding-right: 2rem;
    display: flex;
    flex-direction: row;
    justify-content: center;
    background-image: url("/images/cinesuntem/row-1-col-1.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    align-items: center;
  }
  .cinesuntem__main__img {
    padding: 2rem;
  }
  .cinesuntem__main__text {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: 580px;
  }
  .cinesuntem__second {
    height: 100vh;
    display: flex;
    flex-direction: column;
    padding: 2rem 5rem;
    align-items: center;
    justify-content: center;
    background-image: url("/images/cinesuntem/row-2-col-1.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
  }
  @media (max-width: 720px){
    .cinesuntem__main {
      flex-direction: column;
    }
    .cinesuntem__second {
      padding: 2rem;
    }
    .cinesuntem__valori {
      display: grid;
      grid-template-columns: 1fr 1fr !important;
      grid-template-rows: auto;
      row-gap: 1rem !important;
      column-gap: 1rem !important;
    }
    .cinesuntem__valori__text > h3 {
      font-size: 1rem;
    }
  }
  .cinesuntem__valori__text {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .cinesuntem__valori {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
    row-gap: 2rem;
    column-gap: 2rem;
  }
</style>
