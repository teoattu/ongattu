<script>
  import '../css/global.css'
  export let type = 'primary'
</script>
<button on:click class={type}>
  <slot></slot>
</button>
<style>
  .primary {
    padding: 0.5rem 4rem;
    border-radius: 10000px;
    font-size: 1.5rem;
    font-weight: 600;
    border: none;
    font-family: "Baloo 2";
    background-color: var(--yellow-color);
  }
  .outlined {
    padding: 0.5rem 4rem;
    border-radius: 10000px;
    font-size: 1.5rem;
    font-weight: 600;
    border: 1px solid var(--blue-color);
    color: var(--blue-color);
    background-color: #ffffff00;
    font-family: "Baloo 2";
  }
  .outlined:hover {
    color: #ffffff;
    background-color: var(--blue-color);
  }

</style>