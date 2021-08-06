<template>
  <div class="home">
    <div class="home__container">
      <div class="wrapper__img" data-v-3cc713de="">
        <img src="@/assets/onas.jpg" alt="img" data-v-3cc713de="">
          <span class="text" data-v-3cc713de="">
            <a href="#" class="btn-shine" target="_blank">
              о нас
            </a>
          </span>
      </div>
      <div class="home__text">
        <div class="text__wrapper">
          <div class="about__us">
            <p>
              Являясь партнером-поставщиком инновационных продуктов и
              комплексных решений компания «Group2» занимается модернизацией
              образовательного процесса для колледжей и ВУЗ'ов. <br><br>

              В рамках проекта «Жас Маман», основанного 23 января 2019 года по поручению Первого Президента
              Республики Казахстан Н.А.Назарбаева, нами было оборудовано около 25 колледжей и ВУЗ'ов по международным
              стандартам WorldSkills, современными тренажерами, стендами, учебным оборудованием, необходимым
              для подготовки специалистов, востребованных на республиканском и международном уровне.
            </p>
          </div>
        </div>
      </div>
    </div>
    <Footer class="footer"/>
  </div>
</template>

<script>
import Footer from '@/components/Footer';
export default {
  name: "Home",
  components: {
    Footer,
  },
};
</script>

<style lang="scss" scoped>
    .home {
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    width: 100%;

      .home__container {
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

        .home__text {
        display: flex;
        flex-direction: column;
        position: relative;
        top: -140px;
        margin: 0 auto;
          @media (max-width: 1140px) {
            top: 0;
          }
         background-color: #ffff;
         .text__wrapper {
          //  border: solid 1px;
           padding: 12px;
           margin: 0 auto;
           width: 75%;
           margin-top: 12px;
           @media(max-width: 1140px) {
            margin: 12px;
            width: 90%;
           }
           .about__us {
             line-height: normal;
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
     }
      .footer {
        @media (max-width: 1140px) {
          position: absolute;
          bottom: 0;
        }
      }
  }

</style>
