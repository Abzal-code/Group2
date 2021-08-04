<template>
  <div class="portfolio">
    <div class="portfolio__container">
      <div class="portfolio__header">
        <Blockimage>
        <a href="#" class="btn-shine" target="_blank">
          Портфолио
        </a>
      </Blockimage>
      </div>
      <div class="portfolio__body">
        <div class="block">
          <div class="block__text">
            <p>
              Установлен учебно-тренажерный комплекс <br>
              по изучению обслуживания <br> и ремонта
              подвижного состава для Актюбинского
              колледжа транспорта, коммуникаци и технологий
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project1.png" alt="">
            <img src="../assets/portfolio/project5.png" alt="">
          </div>
        </div>
        <div class="block">
          <div class="block__text">
            <p>
              Поставка носимого комплекса измерения беспроводной связи для Комитета телекоммуникаций Министерства цифрового развития, инноваций и аэрокосмической промышленности Республики Казахстан
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project2.png" alt="">
            <img src="../assets/portfolio/project4.png" alt="">
          </div>
        </div>
        <div class="block">
          <div class="block__text">
            <p>
              Тренажер-имитатор дорожных условий для обучения водителей для Атырауского колледжа транспорта и коммуникации
            </p>
          </div>
          <div class="block__img">
            <img src="../assets/portfolio/project8.png" alt="">
          </div>
        </div>
        <div class="block">
          <div class="block__text">
            <p>
              Установлена видеостена для Республиканской телерадиокорпорация «Казахстан»
            </p>
          </div>
          <div class="block__img"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Blockimage from '@/components/Blockimage'
export default {
  name: "Reviews",
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

  .portfolio {

    .portfolio__container {

      .portfolio__header {

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
    .portfolio__body {
      padding: 10px;
      display: flex;
      flex-direction: column;
      .block {
        display: flex;
        margin-top: 20px;
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
              padding: 10px;
              color: #ffffff;
            }
        }
        .block__img {
          display: flex;
          width: 100%;
          @media (max-width: 1140px) {
            display: inline;
          }
            img {
              @media(max-width: 1140px) {
                width: 100%;
              }
            }
        }
      }
    }
  }
}


</style>
