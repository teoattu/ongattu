<script>
  export let src;
</script>

<div class="card">
  {#if src}
    <img class="card__img" width=320 height=200 src={src} alt="img"/>
  {/if}
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

<style>
.card {
  margin: 1rem;
  max-width: 320px;
  background-color: #fff;
  border-radius: 1rem;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 4fr 1fr 2fr 1fr;
  width: 320px;
  box-shadow: 0px 3px 10px 2px rgba(0,0,0,0.52);
}
.card__img {
  border-top-left-radius: 1rem;
  border-top-right-radius: 1rem;
}
.card__header{
  padding: 0.5rem 1rem;
}
.card__content{
  padding: 0.5rem 1rem;
}
.card__footer {
  padding: 0.5rem 1rem;
}
</style>