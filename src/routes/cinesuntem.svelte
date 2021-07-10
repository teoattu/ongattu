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
    <div class="cinesuntem__main__img">
        {#if windowWidth && windowWidth > 1024}
          <RoundImage src={"/images/cinesuntem/cinesuntem.jpg"} width={windowWidth < 1024 ? 320 : 640} height={windowWidth < 1024 ? 320 : 640}/>
        {:else}
          <img src="/images/cinesuntem/smCine.png" width={320}/>
        {/if}
        
      </div>
    
    <div class="textArea">
      <h2>CINE SUNTEM</h2>
      <p>Înființată în 2014, mai întâi timid, cu activități modeste, de natură socială, dar apoi cu implicare, attu a crescut!</p>
      <p>An de an noi voluntari s-au alăturat misiunii, și au adus cu ei entuziasm, idei, si o puternică dorință de rezolva problemele comunității! De la elevi și studenți, la  profesioniști în diverse domenii de activitate, fiecare a contribuit! </p>
      <p>Iar acum, putem spune cu mândrie că organizăm pe lângă 4 campanii deja cu tradiție - de 1 septembrie, Crăciun, Paște și 1 iunie - și activități de educaționale.</p>
    </div>
  </section>
  <section class="cinesuntem__second">
    <div class="cinesuntem__second__box">
      <h3>Viziune</h3>
      <p>În attu, noi ne dorim să fim o forță care generează schimbări pozitive și durabile pentru societate.</p>
      {#if windowWidth > 1024}
        <svg height="64" width="1">
          <line x1="0" y1="0" x2="0" y2="200" style="stroke:rgb(0,0,0);stroke-width:2" />
          Sorry, your browser does not support inline SVG.
        </svg>
      {:else}
      <!-- 56 comes from padding left+right -->
        <img src="/images/cinesuntem/viziune.jpg" width={windowWidth-56}/>
      {/if}
    </div>
    <div class="cinesuntem__second__box">
      <h3>Misiunea</h3>
      <p>Misiunea noastră este să sprijinim grupurile sociale defavorizate din România prin acțiuni cu scop educațional și social.</p>
      <p>Încă din 2014, proiectele noastre au fost desfășurate de către specialiști în domeniile pedagogiei, psihologiei și sociologiei, având ca scop principal îmbunătățirea vieții persoanelor din mediile defavorizate. </p>
      {#if windowWidth > 1024}
        <svg height="64" width="1">
          <line x1="0" y1="0" x2="0" y2="200" style="stroke:rgb(0,0,0);stroke-width:2" />
          Sorry, your browser does not support inline SVG.
        </svg>
      {:else}
        <img src="/images/cinesuntem/misiune.jpg" width={windowWidth-56}/>
      {/if}
    </div>
    <div class="cinesuntem__second__box">
      <h3>Valori</h3>
      <div class="valori">
        <div class="valori__item">
          <h4>Solidarite</h4>
          <p>Pentru că doar fiind alături de grupurile defavorizate putem să le transformăm viața într-una mai bună.</p>
        </div>
        <div class="valori__item">
          <h4>Umanitate</h4>
          <p>Pentru că doar prin umanitate și compasiune putem înțelege greul prin care grupurile defavorizate trec.</p>
        </div>
        <div class="valori__item">
          <h4>Integritate</h4>
          <p>Pentru că vrem să fim un model de profesionalism în relațiile cu colaboratorii și beneficiarii activităților noastre.</p>
        </div>
        <div class="valori__item">
          <h4>Incluziune</h4>
          <p>Pentru că suntem la fel de puternici pe cât suntem de uniți, și la fel de slabi pe cât de dezbinați.</p>
        </div>
        <div class="valori__item">
          <h4>Implicare</h4>
          <p>Pentru că doar prin acțiunea colectivă putem aduce o schimbarea pozitivă.</p>
        </div>
        <div class="valori__item">
          <h4>Egalitate</h4>
          <p>Pentru că și grupurile defavorizate merită o șansă la o viață mai bună.</p>
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
