<script setup>
import Slider from "./components/Slider.vue";
</script>

<template>
  <div class="container">
    <div class="header">
      <img class="logo" src="./assets/images/logo.png" alt="logo" />
    </div>

    <div class="info">
      <div class="left">
        <h1 class="heading">
          İnternet Üzerinden Kesintisiz Televizyon İzleyin!
        </h1>

        <p class="desc">
          Televizyon yayınlarını geriye alın,istediğiniz programı istediğiniz
          saatte izleyin, hd destekli kanalları izleyin!
        </p>

        <h1 class="fancyHeading">
          <span class="fancyContent">İş Ortaklarımız</span>
        </h1>
        <div class="sliderContainer">
          <Slider />
        </div>
      </div>
      <div class="right">
        <img class="heroImg" src="./assets/images/banner.png" alt="" />
        <div>
          <h1 class="fancyHeading">
            <span class="fancyContent">Uygulamalarımız</span>
          </h1>

          <ul class="buttonGroup">
            <a
              target="_blank"
              href="https://play.google.com/store/apps/details?id=com.makersoft.uyaniktv&hl=tr&gl=US"
              class="shareLink"
            >
              <img
                class="shareImg"
                src="./assets/images/playstore.png"
                alt="googleplay"
              />
            </a>

            <a
              target="_blank"
              href="https://apps.apple.com/us/app/uyan%C4%B1k-tv/id483370868"
              class="shareLink"
            >
              <img
                class="shareImg"
                src="./assets/images/appstore.png"
                alt="appstore"
              />
            </a>

            <a
              target="_blank"
              href="https://play.google.com/store/apps/details?id=tv.euroturk.uyaniktvbox&hl=tr&gl=US"
              class="shareLink"
            >
              <img
                class="shareImg"
                src="./assets/images/tvbox.png"
                alt="tvbox"
              />
            </a>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}

/* header */
.header {
  width: 100%;
  height: 20vh;
  background-color: #fdf9f9;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px,
    rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}

.header::after {
  position: absolute;
  content: " ";
  width: 100%;
  height: 100%;
  background-size: cover;

  z-index: 1;
  opacity: 0.3;
}

.logo {
  width: 150px;
  height: 150px;
  margin: 0 auto;
  z-index: 2;
}

.info {
  display: flex;
  height: 80vh;
  text-align: center;
}

.left {
  flex: 1;
  display: flex;
  row-gap: 2rem;
  flex-direction: column;
}

.heading {
  font-size: 3rem;
  line-height: 50px;
  font-weight: 700;
  margin: 2rem;
  margin-bottom: 0;
}

.desc {
  font-size: 20px;
  margin: 2rem;
  margin-top: 0;
  margin-bottom: 0;
  font-weight: 500;
}

/* fancy heading */

.fancyHeading {
  overflow: hidden;
  text-align: center;
  text-transform: uppercase;
}
.fancyHeading:before,
.fancyHeading:after {
  background-color: #dbd8d8;
  content: "";
  display: inline-block;
  height: 1px;
  position: relative;
  vertical-align: middle;
  width: 50%;
}
.fancyHeading:before {
  right: 0.5em;
  margin-left: -50%;
}
.fancyHeading:after {
  left: 0.5em;
  margin-right: -50%;
}
/* fancy heading */

/* right */
.right {
  flex: 1;
  display: flex;
  row-gap: 2rem;
  flex-direction: column;
  border: 1px solid #dbd8d8;
  padding-top: 2rem;
}

.heroImg {
  width: 500px;
  object-fit: cover;
  margin: 0 auto;
}

.buttonGroup {
  display: flex;
  align-items: center;
  column-gap: 2rem;
  padding: 2rem 2rem;
  justify-content: center;
}

.sliderContainer {
  padding: 2rem;
}

.shareImg {
  width: 200px;
}

.fancyContent {
  padding: 8px;
  border-collapse: collapse;
  border-radius: 8px;
  color: rgb(221, 220, 220);
  font-size: 20px;
  font-weight: 700;
  background-color: #000000;
  background-image: linear-gradient(315deg, #000000 0%, #414141 74%);
}

@media screen and (max-width: 1200px) {
  .info {
    flex-direction: column;
  }
}
</style>
