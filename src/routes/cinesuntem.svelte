<svelte:head>
	<title>Welcome</title>
</svelte:head>

<script>
  import RoundImage from "../components/RoundImage.svelte";
  import "../css/global.css";
</script>

<div class="wrapper">
  <section class="cinesuntem__main">
    <RoundImage src={"/images/cinesuntem/cinesuntem.jpg"}/>
  </section>
</div>

<style>
  .cinesuntem__main {
    height: 100vh;
    padding-top: 64px;
    padding-left: 2rem;
    padding-right: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-image: url("/images/cinesuntem/row-1-col-1.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>