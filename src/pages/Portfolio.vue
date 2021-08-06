<template>
  <div class="portfolio">
    <div class="portfolio__container">
      <div class="wrapper__img" data-v-3cc713de="">
        <img src="@/assets/portfolio.jpg" alt="img" data-v-3cc713de="">
          <span class="text" data-v-3cc713de="">
            <a href="#" class="btn-shine" target="_blank">
              Портфолио
            </a>
          </span>
      </div>
            <div class="portfolio__body">
        <div class="block">
          <div class="block__text">
            <p>
              Установлен учебно-тренажерный комплекс
              по изучению обслуживания <br> и ремонта
              подвижного состава <br> для Актюбинского
              колледжа транспорта, коммуникаци и технологий
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project1/1.png" alt="">
            <img src="../assets/portfolio/project1/2.png" alt="">
          </div>
        </div>
        <div class="block">
          <div class="block__text">
            <p>
              Поставка носимого комплекса измерения беспроводной связи для Комитета телекоммуникаций Министерства цифрового развития, инноваций <br> и аэрокосмической промышленности Республики Казахстан
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project4/1.png" alt="">
            <img src="../assets/portfolio/project4/2.png" alt="">
          </div>
        </div>
        <div class="block">
          <div class="block__text">
            <p>
              Тренажер-имитатор дорожных условий для обучения водителей для Атырауского колледжа транспорта и коммуникации
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project3/1.png" alt="">
            <img src="../assets/portfolio/project3/2.png" alt="">
          </div>
        </div>
        <div class="block">
          <div class="block__text">
            <p>
              Установлена видеостена <br> для Республиканской телерадиокорпорация «Казахстан»
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project2/1.png" alt="">
            <img src="../assets/portfolio/project2/2.png" alt="">
          </div>
        </div>
      </div>
    </div>
    <Footer class="footer"/>
  </div>
</template>

<script>
import Footer from '@/components/Footer'
export default {
  name: "Portfolio",
  components: {
    Footer,
  },
};
</script>

<style lang="scss" scoped>
    .portfolio {
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    width: 100%;

      .portfolio__container {
      display: flex;
      flex-direction: column;
      justify-content: center;

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
        padding: 12px 48px;
        background: linear-gradient(to right, #008DFC 0, #008DFC 10%, #7300ED 20%);
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
          .portfolio__body {
      padding: 10px;
      display: flex;
      flex-direction: column;
      .block {
        display: flex;
        margin: 0 auto;
        border-radius: 20px;
        margin-top: 20px;
        width: 80%;
        background: linear-gradient(#7300ED, #008DFC);
        @media (max-width: 1140px) {
          flex-direction: column;
        }
        .block__text {
          display: flex;
          background-image: linear-gradient(#7300ED, #008DFC);
          @media (max-width: 1140px) {
            width: 100%;
            border-radius: 10px;
            font-size: 15px;
          }
            p {
              padding: 20px;
              color: #ffffff;
            }
        }
        .block__img {
          display: flex;
          flex-direction: row;
          justify-content: flex-end;
          width: 100%;
          @media (max-width: 1140px) {
            display: inline;
          }
            img {
              width: 350px;
              border-radius: 10px;
              margin: 20px;
              @media(max-width: 1140px) {
                width: 100%;
                margin: 0;
                padding: 20px;
                border-radius: 10;
              }
            }
        }
      }
    }
  }
}
</style>
