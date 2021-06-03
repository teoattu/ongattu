<script>
  import Button from "../components/Button.svelte";
import "../css/global.css";
</script>

<svelte:head>
  <title>ONG ATTU HOMEPAGE</title>
</svelte:head>

<div class="wrapper">
  <section class="index__main">
    <h2>Fermentum Posuere</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam lectus
      velit, luctus volutpat enim vel, vulputate tincidunt enim. Sed pretium
      rutrum elit. Ut egestas rhoncus nisi ut ullamcorper.
    </p>
		<div class="index__button__wrapper">
			<Button type="outlined">Cunoaște-ne mai bine</Button>
		</div>
  </section>
</div>

<style>
  .wrapper {
    padding-top: 64px;
    height: 300vh;
    background-image: url("/images/homepageBg.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
  }
  .index__main {
    height: 80vh;
    padding: 1rem 2rem;
		display: flex;
		flex-direction: column;
		justify-content: center;
  }
	.index__main > p {
		max-width: 480px;
	}
@media only screen and (max-width: 720px) {
	h2 {
		font-size: 1.75rem;
	}
	.index__button__wrapper{
		padding-top: 1rem;
	}
}
@media only screen and (min-width: 720px) {
	.index__main {
		padding: 3rem 10rem;
	}
}
</style>
