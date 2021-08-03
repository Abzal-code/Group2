<template>
  <div class="wrapper__img" data-v-3cc713de="">
    <img src="@/assets/it.jpeg" alt="img" data-v-3cc713de="">
      <span class="text" data-v-3cc713de=""><slot></slot></span>
  </div>
</template>

<script>
  export default {
    name: 'Blockimage',
    data() {
      return {
      }
    }
  }
</script>

<style lang="scss" scoped>
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
</style>