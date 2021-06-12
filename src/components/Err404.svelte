<script>
  import '../css/global.css'
</script>

<div class="error">
  <div class="error__message">
    <div class="error__text">
      <h2>OOPS...</h2>
      <h3>Under Construction</h3>
      <a href="/">
        <h4>Back to homescreen</h4>
      </a>
    </div>
  </div>
</div>

<style>
  .error{
    height: 100vh;
    padding-top: 64px;
    background-image: url("/images/error/error404.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
  }
  .error__message {
    width: clamp(300px, 100%, 540px);
    display: flex;
    padding: 3rem;
    flex-direction: column;
    padding-top: 10rem;
    align-items: center;
  }
</style>