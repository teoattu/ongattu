<script>
  import RoundImage from '../components/RoundImage.svelte';
  import Card from '../components/Card.svelte';
  import '../css/global.css';
  import { onMount } from 'svelte';
  import SocialMedia from '../components/SocialMedia.svelte';
  import Modal from '../components/Modal.svelte';
  import Button from '../components/Button.svelte';

  let openModal = false;

  let windowWidth;
  onMount(() => {
    if (typeof window !== undefined) {
      windowWidth = window.innerWidth;
    }
  });
</script>

<svelte:head>
  <title>Impica-te!</title>
</svelte:head>

<div class="imp">
  <section class="imp__main">
    {#if windowWidth && windowWidth > 1024}
      <RoundImage
        src={'/images/implicate/edu.jpg'}
        width={windowWidth < 1024 ? 320 : 640}
        height={windowWidth < 1024 ? 320 : 640}
      />
    {:else}
      <img src="/images/implicate/smEdu.png" width="320"  alt="implica-te"/>
    {/if}
    <div class="imp__main__text">
      <h2>Educație</h2>
      <p>Considerăm că cea mai eficientă cale spre viitorul pe care ni-l dorim are la bază educația. Din nefericire, nivelul educației formale nu este uniform, și de cele mai multe ori nici suficient. Vrem deci să-i ajutăm pe cei care au cea mai multă nevoie, să aibă parte de o educație de bază.
      </p>
    </div>
  </section>
  <section class="imp__second">
    <h3>Descoperă proiectele noastre!</h3>
    {#if windowWidth > 1024}
    {:else}
      <Card src="/images/implicate/Mentorat.jpg">
        <h4 slot="header">Mentorat</h4>
        <p slot="content">Sesiuni de meditații pentru recuperarea materiei și pregătirea pentru examenele naționale pentru un grup de 7 elevi din Prahova și Vaslui.</p>
        <a slot="footer" href="/">Afla mai multe</a>
      </Card>
      <Card src="/images/implicate/superpower.jpeg">
        <h4 slot="header">Discovering my Superpower</h4>
        <p slot="content">O serie de ateliere de dezvoltare personală și orientare în carieră, desfășurate în parteneriat cu TheForgeSpirit, pentru un grup de copii ce provin din medii defavorizate.</p>
        <a slot="footer" href="/">Afla mai multe</a>
      </Card>
      <Card src="/images/implicate/invatamattu.jpeg">
        <h4 slot="header">Să învățăm cu attu!</h4>
        <p slot="content">Activități formale și non-formale desfășurate cu un grup de minimum 6 elevi din școala primară pentru recuperarea materiei și dezvoltarea personală a acestora.</p>
        <a slot="footer" href="/">Afla mai multe</a>
      </Card>
      <Card src="/images/implicate/practicaase.png">
        <h4 slot="header">#InternshipATTU</h4>
        <p slot="content">Un program de internship adresat studenților ASE, pentru dezvoltarea și pregătirea acestora pentru viitoarele lor cariere. </p>
        <a slot="footer" href="/">Afla mai multe</a>
      </Card>
      <Card src="/images/implicate/practicaase.png">
        <h4 slot="header">#InternshipATTU</h4>
        <p slot="content">Un program de internship adresat studenților ASE, pentru dezvoltarea și pregătirea acestora pentru viitoarele lor cariere. </p>
        <a slot="footer" href="/">Afla mai multe</a>
      </Card>
    {/if}
  </section>
</div>

<style lang="scss">
  .imp {
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
      &__text {
        padding-top: 1rem;
      }
      @media (min-width:1024px) {
        flex-direction: row-reverse;
        padding: 80px 135px;
        justify-content: center;
      }
    }
    &__second {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  }
</style>
