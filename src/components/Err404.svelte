<script>
  import '../css/global.css'
</script>

<div class="error">
  <div class="error__message">
    <div class="error__text">
      <h1>OOPS...</h1>
      <h3>Ai ajuns la momentul nepotrivit!</h3>
      <p>Momentan, mai sunt câteva detalii de pus la punct cu această pagină</p>
      <p>dar fii fără griji! Totul va fi gata în curând!</p> 
      <p>Revino puțin mai târziu!</p>
      <br/>
      <p>P.S. Lucrurile bune vin pentru cei ce așteaptă!</p>
    </div>
  </div>
</div>

<style>
  .error__text > h1 {
    font-weight: 800;
  }
  .error__text > h3 {
    font-weight: 600;
  }
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
    /* width: clamp(300px, 100%, 540px); */
    display: flex;
    padding-left: 145px;
    padding-top: 230px;
    flex-direction: column;
    align-items: center;
  }
  @media only screen and (max-width: 720px) {
    .error {
      background-image: url("/images/error/error_mobile.png"); 
    }
    .error__message {
      padding-left: 55px;
      padding-right: 55px;
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