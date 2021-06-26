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
  <title>Activitati</title>
</svelte:head>
<div class="social">
  <section class="social__main">
    <div class="social__main__text">
      <div>
        <h2>Social</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
      </div>
    </div>
    <div class="cinesuntem__main__img">
      <RoundImage
        src={"/images/social/Social.jpg"}
        width={windowWidth < 720 ? 320 : 640}
        height={windowWidth < 720 ? 320 : 640}
      />
    </div>
  </section>
</div>

<style lang="scss">
  .social {
    width: 100%;
    &__main {
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
      @media (max-width: 1024px) {
        flex-direction: column;
      }
      &__img {
        padding: 2rem;
      }
      &__text {
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        max-width: 580px;
      }
    }
  }
</style>
