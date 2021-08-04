<template>
  <div class="partners">
    <div class="partners__container">
      <Blockimage>
        <a href="#" class="btn-shine" target="_blank">
          Партнеры
        </a>
      </Blockimage>
      <div class="partners__wrapper">
        <div class="partners__img">
          <img src="@/assets/oppo.png" alt="oppo">
          <img src="@/assets/uchteh.png" alt="учтех">
          <img src="@/assets/imakr.png" alt="imakr">
          <img src="@/assets/vertiv.png" alt="vertiv">
          <img src="@/assets/citrix.png" alt="citrix">
          <img src="@/assets/kh.png" alt="khproductions">
          <img src="@/assets/vce.png" alt="vce">
          <img src="@/assets/boch.png" alt="bosch">
          <img src="@/assets/acer.png" alt="acer">
          <img src="@/assets/forward.png" alt="forward">
          <!-- <img src="@/assets/wallix.png" alt="wallix"> -->
          <img src="@/assets/dell.png" alt="dell">
          <img src="@/assets/lenovo.png" alt="lenovo">
          <img src="@/assets/proma.png" alt="proma">
          <img src="@/assets/d-link.png" alt="d-link">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Blockimage from '@/components/Blockimage'
export default {
  name: "Partners",
  components: {
    Blockimage,
  },
};
</script>

<style lang="scss" scoped>
body {
    background: black
  font-family 'Poppins', sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
}
  .partners {

    .partners__container {

      .btn-shine {
        position: absolute;
        transform: translate(-50%,-50%);
        background: linear-gradient(to right, #008DFC 0, #008DFC 10%, #7300ED 20%);
        padding: 12px 48px;
        color: #ffffff;
        background-position: 0;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        animation: shine 3s infinite linear;
        animation-fill-mode: forwards;
        -webkit-text-size-adjust: none;
        font-weight: 600;
        font-size: 46px;
        text-decoration: none;
        white-space: nowrap;

        @keyframes shine {
          0% {
            background-position: 0
          }

          60% {
            background-position: 180px
          }


          100% {
            background-position: 360px
          }
        }
      }

      .partners__wrapper {
        display: flex;
        flex-direction: row;
        justify-content: center;
        margin: 45px;
        @media (max-width: 1140px) {
          flex-direction: column;
        }
        .partners__text {
          display: flex;
        }
        .partners__img {
          display: flex;
          flex-wrap: wrap;
          justify-content: center;
          height: 100%;
          margin-left: auto;
          margin-right: auto;
          @media (max-width: 1140px) {
            width: 100%;
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            justify-content: space-around;
          }
          img {
            display: flex;
            margin: 50px;
            @media (max-width: 1140px) {
              width: 20%;
              height: 20%;
              margin: 25px;
            }
          }
        }
      }
    }
  }


</style>
