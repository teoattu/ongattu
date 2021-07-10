<script>
  import RoundImage from "../components/RoundImage.svelte";
  import Card from "../components/Card.svelte";
  import "../css/global.css";
  import SocialMedia from "../components/SocialMedia.svelte";
  import { onMount } from "svelte";

  let windowWidth;
  onMount(() => {
    if (typeof window !== undefined) {
      windowWidth = window.innerWidth;
    }
  });
</script>

<svelte:head>
  <title>Activitati</title>
</svelte:head>
<div class="activitati">
  <section class="activitati__main">
    <div class="cinesuntem__main__img">
        {#if windowWidth && windowWidth > 1024}
          <RoundImage src={"/images/activitati/cefacem.jpg"} width={windowWidth < 1024 ? 320 : 640} height={windowWidth < 1024 ? 320 : 640}/>
        {:else}
          <img src="/images/activitati/smCefacem.png" width="320"/>
        {/if}
      </div>
    <div class="textArea">
      <h2>CE FACEM</h2>
      <p>Toate proiectele și activitățile noastră au o componentă socială și educațională. Încercăm, cu alte cuvinte, să echilibrăm cumva balanța și să-i ajutăm pe cei în nevoie.</p>
      {#if windowWidth > 1024}
        <p>Printre proiectele noastre anuale se regăsesc :</p>
        <p>•  Campaniile regulate în comunități dezavantajate - 1 iunie, 1 septembrie, Crăciun și Paște - unde oferim produse de primă necesitate dar și scurte sesiuni de consiliere;</p>
        <p>•  Mentorat pentru elevii din an terminal;</p>
        <p>•  Vizite la bătrâni singuri;</p>
        <p>Cu toate acestea, anul acesta am avut proiecte noi și diferite, bazate pe educație, orientare în carieră și descoperirea abilităților proprii!</p>
      {/if}
    </div>
  </section>
  <section class="activitati__second">
    <h3>Descopera Activitatile Noastre</h3>
    <div class="activitati__second__cards">
      <Card src={"/images/activitati/edu.jpg"}>
        <h4 slot="header">Educație</h4>  
        <p style="font-size: 1.125rem;" slot="content">Considerăm că cea mai eficientă cale spre viitorul pe care ni-l dorim are la bază educația. Din nefericire, nivelul educației formale nu este uniform, și de cele mai multe ori nici suficient. Vrem deci să-i ajutăm pe cei care au cea mai multă nevoie să aibă parte de o educație de bază.</p>
        <a slot="footer" href="/">Afla mai multe</a>
      </Card>
      <Card src={"/images/activitati/social.jpg"}>
        <h4 slot="header">Social</h4>
        <p style="font-size: 1.125rem;" slot="content">Viața nu e dreaptă, dar asta nu înseamnă că noi nu putem da o mână de ajutor! Fie că vine vorba de produse alimentare, articole de îmbrăcăminte, sau pur și simplu puțin ajutor în gospodărie, noi suntem mereu pregătiți să venim în ajutorul celor care au nevoie.</p>
        <a slot="footer" href="/">Afla mai multe</a>

      </Card>

    </div>
  </section>
  <SocialMedia/>
</div>

<style lang="scss">
  .textArea {
    padding: 1rem;
    padding-left: 0;
  }

  .activitati {
    padding: 1rem 2rem;
    padding-top: 64px;
    background-image: url("/images/activitati/background.png");
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
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      h3 {
        text-align: center;
        @media (min-width:1024px) {
          padding: 1rem;
        }
      }
      &__cards {
        display: flex;
        flex-direction: column;
        align-items: center;
        @media (min-width:1024px) {
          width: 100%;
          flex-direction: row;
          justify-content: space-evenly;
        }
      }
    }
  }
</style>
