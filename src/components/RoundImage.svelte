<script>
  import '../css/global.css'
  export let src;
  export let width = 620;
  export let height = 620;
</script>

<img class="rounded__image" src={src} alt="img" width={width} height={height}/>

<style>
  .rounded__image {
    border-radius: 50%;
    object-fit: cover;
  }
</style>