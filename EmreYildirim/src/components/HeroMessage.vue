<template>
  <nav class="navbar">
      <div class="navbar__logo"><img class="navbar__logo-image" src="../assets/images/logo.png"  alt=""></div>
  </nav>

  <div class="container">
    <div class="selection">
      <h1 class="firstPromotion">Software Engineer <br>EMRE YILDIRIM</h1>
    </div>
  </div>
  
  <div class="footer">
      <a href="mailto:ia.emreyildirim@gmail.com"><img src="../assets/icons/mail.png" alt="Mail" class="footer-icon"></a>
      <a href="https://github.com/emreyildrm1?tab=overview&from=2024-08-01&to=2024-08-01"><img src="../assets/icons/github.png" alt="" class="footer-icon"></a>
      <a href="https://www.linkedin.com/in/emre-yildirimm/"><img src="../assets/icons/linedin.png" alt="" class="footer-icon"></a>
  </div>
</template>
<script>
export default {
  name: 'HeroMessage',
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Audiowide&display=swap');

//sass kısayolları

$title-color: rgb(190, 190, 190);
$large-font: 65px;
$medium-font: 50px;
$small-font: 30px;
$icon-nomal-width: 36px;
$icon-small-width: 30px;
$logo-width: 100px;
$romotion-font-family: 'Audiowide', sans-serif;


// Mixin'ler
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
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
  margin-bottom: 50px;
}

.footer-icon{
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
  
  .footer-icon{
    margin-left: 15px;
  }
}

/* Tabletler için */
@media (min-width: 601px) and (max-width: 1024px) {
  
  .firstPromotion {
    font-size: $medium-font;
  }
  .footer {
    .footer-icon{
      width: $icon-nomal-width;
    }
  }
}
</style>
