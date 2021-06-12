<svelte:head>
	<title>Cine Suntem</title>
</svelte:head>

<script>
  import RoundImage from "../components/RoundImage.svelte";
  import "../css/global.css";
</script>

<div class="wrapper">
  <section class="cinesuntem__main">
    <div class="cinesuntem__main__text">
      <h2>CINE SUNTEM</h2>
      <p>SOME TEXT</p>
    </div>
    <div class="cinesuntem__main__img">
      <RoundImage src={"/images/cinesuntem/cinesuntem.jpg"}/>
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
    padding-top: 1rem;
    padding-left: 19rem;
  }

</style>