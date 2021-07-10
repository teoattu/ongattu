<svelte:head>
	<title>Doneaza</title>
</svelte:head>
<script>
  import Button from '../components/Button.svelte';
</script>
<div class="doneaza">
  <section class="doneaza__main">
    <h2>Când donezi pentru o cauza nobilă, câștigi mai mult decât pierzi </h2>
    <p>îți mulțumim că ne ești alături și contribui la fericirea și viitorul grupurilor defavorizate</p>
    <a href="https://secure.mobilpay.ro/buy-product/c8en7ker"><Button type="outlined">DONEAZA ACUM</Button></a>
   
  </section>
</div>

<style lang="scss">
  .doneaza {
    padding-top: 64px;
    // background-image: url("/images/contact/background.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    &__main {
      display: flex;
      padding: 80px 1rem;

      flex-direction: column;
      align-items: center;
      justify-content: center;
      @media (min-width:1024px) {
        padding: 80px 135px;
      }
    }
  }
</style>