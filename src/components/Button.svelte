<script>
  import '../css/global.css'
  export let type = 'primary'
</script>
<button on:click class={type}>
  <slot></slot>
</button>
<style>
  .primary {
    padding: 0.5rem 2rem;
    border-radius: 10000px;
    font-size: 1rem;
    font-weight: 600;
    border: none;
    font-family: "Baloo 2";
    background-color: var(--main-yellow-color);
  }
  .outlined {
    padding: 0.5rem 2rem;
    border-radius: 10000px;
    font-size: 1rem;
    font-weight: 600;
    border: 1px solid var(--main-blue-color);
    color: var(--main-blue-color);
    background-color: #ffffff00;
    font-family: "Baloo 2";
  }
  .outlined:hover {
    color: #ffffff;
    background-color: var(--main-blue-color);
  }

</style>