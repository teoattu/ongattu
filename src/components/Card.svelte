<script>
  export let src;
  import { onMount } from "svelte";

  let windowWidth;
  onMount(() => {
    if (typeof window !== undefined) {
      windowWidth = window.innerWidth;
    }
  });
</script>

<div class="card">
  {#if src}
    <div class="card__img" style="background-image: url({src});">
    </div>
    {/if}
  <!-- {#if src}
    <img class="card__img" src={src} alt="img"/>
  {/if} -->
  <div class="card__header">
    <slot name="header"></slot>
  </div>
  <div class="card__content">
    <slot name="content"></slot>
  </div>
  <div class="card__footer">
    <slot name="footer"></slot>
  </div>
</div>

<style lang="scss">
.card {
  margin: 1rem;
  background-color: #fff;
  border-radius: 1rem;
  display: flex;
  flex-direction: column;
  width: 320px;
  box-shadow: 0px 3px 10px 2px rgba(0,0,0,0.52);
  // max-height: 720px;
  @media (min-width: 1024px) {
    width: 500px;
  }
}
.card__img {
  width: 100%;
  height: 200px;
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
  border-top-left-radius: 1rem;
  border-top-right-radius: 1rem;
  @media (min-width: 1024px) {
    height: 300px;
    
  }
  /* width: 100%;
  height: 60%;
  border-top-left-radius: 1rem;
  border-top-right-radius: 1rem;
  object-fit: cover; */

}
.card__header{
  padding: 0.5rem 1rem;
}
.card__content{
  padding: 0.5rem 1rem;
  flex-grow: 1;

}
.card__footer {
  padding: 0.5rem 1rem;
  justify-self: flex-end;
  margin-bottom: 20px;
}
</style>