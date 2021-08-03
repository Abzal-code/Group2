<template>
  <div class="footer">
    <div class="footer__wrapper">
      <div class="copyright">
        <a href="#">&copy; Copyright 2021 Group2</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Footer'
  }
</script>

<style lang="scss" scoped>
  .footer {
      width: 100%;
      background-image: linear-gradient(#7300ED, #008DFC);
    .footer__wrapper {
      margin-left: 150px;
      padding: 15px;
      @media(max-width: 1140px) {
        margin: 0;
      }
      .copyright {
        a {
          margin-right: 12px;
          text-decoration: none;
          color: #ffffff;
        }
      }
    }
  }
</style>