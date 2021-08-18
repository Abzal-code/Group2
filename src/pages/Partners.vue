<template>
  <div class="partners">
    <div class="partners__container">
      <div class="wrapper__img" data-v-3cc713de="">
        <img src="@/assets/partnery.jpg" alt="img" data-v-3cc713de="">
          <span class="text" data-v-3cc713de="">
            <a href="#" class="btn-shine" target="_blank">
              партнеры
            </a>
          </span>
      </div>
      <div class="partners__wrapper">
        <div class="partners__img">
          <img src="@/assets/oppo.png" alt="oppo">
          <img src="@/assets/uchteh.png" alt="учтех">
          <img src="@/assets/imakr.png" alt="imakr">
          <img src="@/assets/dell.png" alt="dell">
          <img src="@/assets/citrix.png" alt="citrix">
          <img src="@/assets/kh.png" alt="khproductions">
          <img src="@/assets/vce.png" alt="vce">
          <img src="@/assets/boch.png" alt="bosch">
          <img src="@/assets/acer.png" alt="acer">
          <img src="@/assets/forward.png" alt="forward">
          <!-- <img src="@/assets/wallix.png" alt="wallix"> -->
          <img src="@/assets/vertiv.png" alt="vertiv">
          <img src="@/assets/lenovo.png" alt="lenovo">
          <img src="@/assets/proma.png" alt="proma">
          <img src="@/assets/d-link.png" alt="d-link">
        </div>
      </div>
      <div class="img_link">
        <div class="link_wrapper">
          <a href="https://www.coreldraw.com/en/product/coreldraw/2021.html?x-vehicle=ppc_brkws&gclid=Cj0KCQjwvO2IBhCzARIsALw3ASo_q0ud8gTRaldwMgBke22cJ1DKTMzYVSEYkYgt2yPaErckzCIB5JIaAkQ-EALw_wcB">
            <img src="@/assets/first.png" alt="">
            <img src="@/assets/second.jpeg" alt="">
          </a>
        </div>
      </div>
    </div>
    <Footer class="footer"/>
  </div>
</template>

<script>
import Footer from '@/components/Footer'
// @ is an alias to /src
export default {
  name: "Partners",
  components: {
    Footer,
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
      .wrapper__img {
      display: flex;
      position: relative;
      width: 100%;
      align-content: center;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      img {
        display: flex;
        width: 100%;
        margin: 0 auto;
        background: rgba(0, 0, 0, 0.5);
        opacity: 0.5;
      }
      span {
        display: flex;
        position: absolute;
        font-style: normal;
        font-weight: bold;
        font-size: 27px;
        background: rgba(0, 0, 0, 0.5);
        // color: #fafafa;
        line-height: 35px;
        text-align: center;
        text-transform: uppercase;
        padding: 0 5px;
        @media(max-width: 1140px) {
          font-family: Raleway;
          font-size: 15px;
          line-height: 15px;
          margin-top: 35px;
        }
      }
  }

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
        @media (max-width: 1140px) {
          font-size: 35px;
        }

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
          align-items: center;
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
            margin: 45px;
            // width: 70px;
            @media (max-width: 1140px) {
              margin: 25px;
            }
          }
        }
      }
      .img_link {
        width: 100%;
        .link_wrapper {
          width: 100%;
          display: flex;
          a {
            display: flex;
            flex-direction: column;
            width: 100%;
            img {
              display: flex;
              width: 100%;
            }
          }
        }
      }
    }
  }



</style>
