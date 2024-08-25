<template>
  <div class="glass-effect">
    <nav class="navbar">
        <div class="navbar__logo"><img class="navbar__logo-image" src="../assets/images/logo.png"  alt=""></div>
    </nav>

    <div class="container">
      <div class="selection">
        <h1 class="firstPromotion">Software Engineer <br>EMRE YILDIRIM</h1>
      </div>
    </div>

    <div class="footer">
        <a href="mailto:ia.emreyildirim@gmail.com" class="footer__box"><img src="../assets/icons/mail.png" alt="Mail" class="footer__box-icon"></a>
        <a href="https://github.com/emreyildrm1?tab=overview&from=2024-08-01&to=2024-08-01" class="footer__box"><img src="../assets/icons/github.png" alt="" class="footer__box-icon"></a>
        <a href="https://www.linkedin.com/in/emre-yildirimm/" class="footer__box"><img src="../assets/icons/linedin.png" alt="" class="footer__box-icon"></a>
    </div>
</div>

</template>
<script>
export default {
  name: 'HeroMessage',
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Anek+Devanagari:wght@100..800&display=swap');

//sass

$title-color: rgb(48, 48, 48);
$large-font: 60px;
$medium-font: 50px;
$small-font: 30px;
$icon-nomal-width: 36px;
$icon-small-width: 30px;
$logo-width: 100px;
$romotion-font-family: 'Audiowide', sans-serif;


// Mixin
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.glass-effect{
  
  display: flex;
  justify-content: space-between;
  flex-wrap: nowrap;
  flex-direction: column;
  align-items: center;

  background: rgba(255, 255, 255, 0.1); 
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.5); 
  padding: 20px;
  width: 90%;
  height: 85vh;
  margin-top: 5vh;
}
// Navbar
.navbar {
  @include flex-center;
  height: auto;
  padding-top: 40px;

  &__logo-image {
    width: $logo-width;
    border-radius: 50px;
  }
}

/* content */


.firstPromotion{
  align-items: start;

  font-size: $large-font;
  font-weight: 100;
  color: $title-color;
  font-family: 'Audiowide', sans-serif;
  
}

.container{
  margin: auto;
  display: contents;
}
.selection{
  display: flex;

  width: 100%;
  margin: auto;
}






/* footer */

.footer{
  display: flex;
  justify-content: space-around;

  width: 80%;
  color: white;
}

.footer__box{
  display: flex;
  margin-inline: 30px;
}


.footer__box-icon{
  width: $icon-nomal-width;
  border-radius: 10px;
}





/* Mobil cihazlar için */
@media (max-width: 600px) {
  
  .firstPromotion {
    font-size: $small-font;
  }
  .footer {
    .footer-icon{
      width: $icon-small-width;
    }
  }
  
  .footer__box-icon{
    margin-left: 15px;
  }
}

/* Tabletler için */
@media (min-width: 601px) and (max-width: 1024px) {
  
  .firstPromotion {
    font-size: $medium-font;
  }
  .footer {
    .footer__box-icon{
      width: $icon-nomal-width;
    }
  }
}
</style>
