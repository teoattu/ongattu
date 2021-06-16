<script>
  import '../css/global.css'
</script>

<div class="error">
  <div class="error__message">
    <div class="error__text">
      <h1>OOPS...</h1>
      <h3>Ai ajuns la momentul nepotrivit!</h3>
    </div>
  </div>
</div>

<style>
  .error{
    height: 100vh;
    padding-top: 64px;
    background-image: url("/images/error/error_fundal.png");
    background-position: top;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
  }
  .error__message {
    width: clamp(300px, 100%, 540px);
    display: flex;
    padding: 3rem;
    padding-top: 230px;
    flex-direction: column;
    align-items: center;
  }
  @media only screen and (max-width: 720px) {
    .error {
      background-image: url("/images/error/error_mobile.png"); 
    }
    .error__message {
      padding-top: 300px;
    }
    .error__text > h1 {
      font-size: 3rem;
    }
    .error__text > h3 {
      font-size: 1.5rem;
    }
  }
</style>