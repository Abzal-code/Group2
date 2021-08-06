<template>
  <div class="reviews">
    <div class="reviews__container">
      <div class="wrapper__img" data-v-3cc713de="">
        <img src="@/assets/otzyvy.jpg" alt="img" data-v-3cc713de="">
          <span class="text" data-v-3cc713de="">
            <a href="#" class="btn-shine" target="_blank">
              Отзывы
            </a>
          </span>
      </div>
    </div>
    <Footer class="footer"/>
  </div>
</template>

<script>
import Footer from '@/components/Footer'
// @ is an alias to /src
export default {
  name: "Reviews",
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
  .reviews {

    .reviews__container {

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
    }
        .footer {
        @media (max-width: 1140px) {
          position: absolute;
          bottom: 0;
        }
      }
  }

</style>
