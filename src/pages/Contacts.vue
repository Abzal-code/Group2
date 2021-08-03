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
        
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Blockimage from '@/components/Blockimage'
export default {
  name: "Contacts",
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
  .contacts {

    .contacts__container {

      .btn-shine {
        position: absolute;
        transform: translate(-50%,-50%);
        padding: 12px 48px;
        color: #ffffff;
        background: linear-gradient(to right, #FEEA10 0, #FCCE0E 10%, #008D1C 20%);
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
  }

</style>
