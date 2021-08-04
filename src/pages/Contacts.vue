<template>
  <div class="contacts">
      <div class="contacts__container">
        <Blockimage>
          <a href="#" class="btn-shine" target="_blank">
            Контакты
          </a>
        </Blockimage>
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
  </div>
</template>

<script>
import DG from "2gis-maps";
// @ is an alias to /src
import Blockimage from '@/components/Blockimage'
export default {
  data() {
    return {
      map: null,
    }
  },
  name: "Contacts",
  components: {
    Blockimage,
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
body {
    background: black
  font-family 'Poppins', sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
}
  .contacts {

    .contacts__container {

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
  }

</style>
