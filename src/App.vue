<template>
  <div class="wrapper">
      <navigation class="nav"/>
    <div class="main">
      <router-view v-slot="{ Component }" >
        <transition
        enter-active-class="animate__animated animate__fadeInRight"
        leave-active-class="animate__animated animate__fadeOutLeft"
        mode="out-in">
        <component :is="Component"/>
        </transition>
      </router-view>
    </div>
    <Footer class="footer"/>
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    Navigation,
    Footer,
  },
  data() {
    return {
      //  transitionName: 'slide-left'
    }
  },
  // watch: {
  //   $route(to, from) {
  //     const toDepth = to.path.split('/').length
  //     const fromDepth = from.path.split('/').length
  //     this.transitionName = toDepth < fromDepth ? 'slide-right' : 'slide-left'
  //   }
  // }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@200;300;700&display=swap');
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;

  html, body {
    height: 100%;

    .wrapper {
      display: flex;
      flex-direction: column;
      min-height: 100%;
      .main {
        // height: 100%;
        // position: relative;
        flex: 1 0 auto;
      }

      .footer {
        display: flex;
        // margin-top: auto;
        flex: 0 0 auto;
        @media(max-width: 1140px) {
          // position: absolute;
          // bottom: 0;
        }
      }
    }
  }

  .fade-enter-from,
  .fade-enter-to {
    opacity: 0;
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity .5s ease-out;
  }
}

</style>
