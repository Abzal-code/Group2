<template>
  <div class="contacts">
      <div class="contacts__container">
        <div class="wrapper__img" data-v-3cc713de="">
          <img src="@/assets/it.jpeg" alt="img" data-v-3cc713de="">
            <span class="text" data-v-3cc713de="">
              <a href="#" class="btn-shine" target="_blank">
                Контакты
              </a>
            </span>
        </div>
      </div>
      <div class="contacts__wrapper">
        <div class="map">
          <div id="map" style="width:600px; height:150px;"></div>
        </div>
        <div class="contacts__info">
          <p>
            Адрес ТОО «GROUP 2» <br>
            РК, г.Алматы, пр. Достык, здание 210 <br>
            Тел.+7(775)825-15-58 <br>
            Почта: info@group2.kz
          </p>
        </div>
      </div>
    <Footer class="footer"/>
  </div>
</template>

<script>
import Footer from '@/components/Footer'
import DG from "2gis-maps";
// @ is an alias to /src
export default {
  data() {
    return {
      map: null,
    }
  },
  name: "Contacts",
  components: {
    Footer,
  },
  mounted() {
    var map;

    DG.then(function () {
        map = DG.map('map', {
            center: [43.2299951, 76.9608712],
            zoom: 16
        });

        DG.marker([43.2299951, 76.9608712]).addTo(map).bindPopup('Адрес ТОО «GROUP 2» РК, г.Алматы, пр. Достык, здание 210');
    });
  },
};
</script>

<style lang="scss" scoped>

  .contacts {

    .contacts__container {

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
        color: #ffffff;
        background: linear-gradient(to right, #008DFC 0, #008DFC 10%, #7300ED 20%);
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
    .contacts__wrapper {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      @media (max-width: 1140px) {
        flex-direction: column;
      }
      .map {
        display: flex;
        margin: 30px;
        @media (max-width: 1140px) {
          width: 100%;
        }
      }
      .contacts__info{
        display: flex;
        line-height: 1.5;
      }
    }
        .footer {
        display: flex;
        // margin-top: auto;
        flex: 0 0 auto;
        @media(max-width: 1140px) {
          position: absolute;
          bottom: 0;
        }
      }
  }

</style>
