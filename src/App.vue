<template>
    <navigation class="nav"/>
    <router-view v-slot="{ Component }">
      <transition
      enter-active-class="animate__animated animate__fadeInRight"
      leave-active-class="animate__animated animate__fadeOutLeft"
      mode="out-in">
        <component :is="Component"/>
      </transition>
    </router-view>
    <Footer/>
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
