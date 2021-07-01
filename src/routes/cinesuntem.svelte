<script>
  import RoundImage from "../components/RoundImage.svelte";
  import SocialMedia from "../components/SocialMedia.svelte"
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

<div class="cinesuntem">
  <section class="cinesuntem__main">
    {#if windowWidth }
    <div class="cinesuntem__main__img">
      <RoundImage src={"/images/cinesuntem/cinesuntem.jpg"} width={windowWidth < 1024 ? 320 : 640} height={windowWidth < 1024 ? 320 : 640}/>
    </div>
    {/if}
    <div class="textArea">
      <h2>CINE SUNTEM</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit necessitatibus quae ullam ex dolorum incidunt officiis asperiores. Blanditiis quas vel dolorem nihil quibusdam? Perspiciatis impedit ipsum quas neque itaque enim beatae, officiis omnis nemo corporis error odio quibusdam minus alias laboriosam placeat, assumenda nulla dolorem id quasi. Dolorem, placeat fugit.</p>
    </div>
  </section>
  <section class="cinesuntem__second">
    <div class="cinesuntem__second__box">
      <h3>Viziune</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas laboriosam maxime aspernatur.</p>
      {#if windowWidth > 1024}
        <svg height="64" width="1">
          <line x1="0" y1="0" x2="0" y2="200" style="stroke:rgb(0,0,0);stroke-width:2" />
          Sorry, your browser does not support inline SVG.
        </svg>
      {:else}
      <!-- 56 comes from padding left+right -->
        <img src="/images/cinesuntem/cinesuntem.jpg" width={windowWidth-56}/>
      {/if}
    </div>
    <div class="cinesuntem__second__box">
      <h3>Misiunea</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas laboriosam maxime aspernatur.</p>
      {#if windowWidth > 1024}
        <svg height="64" width="1">
          <line x1="0" y1="0" x2="0" y2="200" style="stroke:rgb(0,0,0);stroke-width:2" />
          Sorry, your browser does not support inline SVG.
        </svg>
      {:else}
        <img src="/images/cinesuntem/cinesuntem.jpg" width={windowWidth-56}/>
      {/if}
    </div>
    <div class="cinesuntem__second__box">
      <h3>Valori</h3>
      <div class="valori">
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, quia!</p>
        </div>
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, quia!</p>
        </div>
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, quia!</p>
        </div>
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, quia!</p>
        </div>
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, quia!</p>
        </div>
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, quia!</p>
        </div>
      </div>
    </div>
  </section>
  <section class="cinesuntem__parteneri">
    <h3>Partenerii nostri</h3>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ad, ut.</p>
    {#if windowWidth > 1024}
      <img src="/images/cinesuntem/lgSponsori.png" width="720"/>
    {:else}
      <img src="/images/cinesuntem/smSponsori.png" width="360"/>
    {/if}
  </section>
  <SocialMedia/>
</div>

<style lang="scss">
   @media (max-width:1024px) {
    p {
      font-size: 1.25rem;
      }
    h3 {
      font-size: 2rem;
    }
    h4 {
      font-size: 1.75rem;
    }
  }
  .textArea {
    padding: 1rem;
    padding-left: 0;
  }
  .cinesuntem {
    padding: 1rem 2rem;
    padding-top: 64px;
    background-image: url("/images/cinesuntem/background.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;

    &__main {
      display: flex;
      padding-top: 80px;
      flex-direction: column;
      align-items: center;
      justify-content: center;
     
      h2 {
        font-size: 3rem;
        @media (min-width: 1024px) {
          font-size: 4rem;
        }
      }
      
      @media (min-width:1024px) {
        flex-direction: row-reverse;
        padding: 80px 135px;
        justify-content: center;
      }
    }
    &__second {
      padding-top: 2rem;
      
      display: flex;
      flex-direction: column;
      @media (min-width:1024px) {
        align-items: center;
      }
      &__box {
        padding-top: 1rem;
        display: flex;
        flex-direction: column;
        @media (min-width:1024px) {
          align-items: center;
          justify-content: center;
          text-align: center;
        }
      }
    }
    &__parteneri {
      padding-top: 2rem;
      display: flex;
      flex-direction: column;
      @media (min-width:1024px) {
        align-items: center;
      }
    }
  }  

  .valori {
    padding-top: 1rem;
    display:grid;
    grid-template-columns: 1fr;
    grid-template-rows: 6fr;
    @media (min-width:1024px) {
      grid-template-columns: repeat(3,1fr);
      grid-template-rows: repreat(2,1 fr);
      row-gap: 3rem;
      column-gap: 4rem;
    }
    &__item{
      h4 {
        color: var(--blue-color)
      }
    }
  }

</style>
