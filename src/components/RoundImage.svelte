<script>
  import '../css/global.css'
  export let src;
</script>

<img class="rounded__image" src={src} alt="img"/>

<style>
  .rounded__image {
    border-radius: 50%;
    width: 620px;
    height: 620px;
    object-fit: cover;
  }
</style>