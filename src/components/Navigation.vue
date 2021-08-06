<template>
    <header :class="{'scrolled-nav': scrollPosition}">
      <nav>
        <div class="branding">
          <img class="desktop" src="@/assets/group.png" alt="logo">
          <img class="mobile" src="@/assets/group.png" alt="logo">
        </div>
        <ul v-show="!mobile" class="navigation">
          <li><router-link class="link" to="/">О нас</router-link></li>
          <li><router-link class="link" to="/portfolio">Портфолио</router-link></li>
          <li><router-link class="link" to="/reviews">Отзывы</router-link></li>
          <li><router-link class="link" to="/partners">Партнёры</router-link></li>
          <li><router-link class="link" to="/contacts">Контакты</router-link></li>
        </ul>
        <div class="icon">
          <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars" :class="{'icon-active': mobileNav}"></i>
        </div>
        <transition name="mobile-nav">
          <ul v-show="mobileNav" class="dropdown-nav">
            <li><router-link class="link" to="/">О нас</router-link></li>
            <li><router-link class="link" to="/portfolio">Портфолио</router-link></li>
            <li><router-link class="link" to="/reviews">Отзывы</router-link></li>
            <li><router-link class="link" to="/partners">Партнёры</router-link></li>
            <li><router-link class="link" to="/contacts">Контакты</router-link></li>
          </ul>
        </transition>
        <div class="icon">
          <i @click="toggleMobileNav" v-show="mobile" class="far fa-bars" :class="{'icon-active': mobileNav}"></i>
        </div>
      </nav>
    </header>
</template>

<script>
export default {
  name: "navigation",
  data() {
    return {
      scrollPosition: null,
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    }
  },
  created() {
    window.addEventListener('resize', this.checkScreen);
    this.checkScreen();
  },
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return
      }
      this.mobile = false;
      this.mobileNav = false;
      return
    }
  },
};
</script>

<style lang="scss" scoped>

  header {
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: 0.5s ease all;
    color: #000000;
    @media(max-width: 1140px) {
      //position: fixed;
      width: 100%;
    }

    .mobile{
      display: none;
    }
    @media(max-width: 1140px) {
      color: #8A2BE2;
      .mobile{
        display: block;
      }
      .desktop {
        display: none;
      }
    }


    nav {
      position: relative;
      display: flex;
      flex-direction: row;
      padding: 12px 0;
      transition: .5s ease all;
      width: 100%;
      margin: 0 auto;
      // background-color: #ffffff;
      @media(min-width: 1140px) {
        max-width: 1140px;
      }

      ul,
      .link {
        font-weight: 700;
        color: #000000;
        width: 100%;
        list-style: none;
        text-decoration: none;
        // background-color: #ffffff;
      }

      li {
        padding: 5px;
        margin-left: 16px;
        // background-color: #ffffff;
      }

      .link {
        // font-size: 20px;
         font-size: 1.1rem;
        // width: 100%;
        transition: 0.5s ease all;
        padding-bottom: 4px;
        border-bottom: 2px solid transparent;

        &:hover, &.router-link-exact-active {
          color: #262626;
          border-color: #7300ED;
        }
      }

        .branding {
          display: flex;
          align-items: center;
          max-width: 200px;
          img {
            // background-color: #ffffff;
            width: 100%;
            transition: 0.5s ease all;
            @media(max-width: 1140px) {
              width: 75%;
            }
          }
        }

      .navigation {
        display: flex;
        align-items: center;
        flex: 1;
        justify-content: flex-end;
      }

      .icon {
        display: flex;
        align-items: center;
        position: absolute;
        top: 0;
        right: 24px;
        height: 100%;

        i {
          cursor: pointer;
          font-size: 24px;
          transition: .8s ease all;
        }
      }

      .icon_active {
        transform: rotate(188deg);
      }

      .dropdown-nav {
        display: flex;
        flex-direction: column;
        position: fixed;
        width: 100%;
        // max-width: 250px;
        // height: 100%;
        background-color: #262626;
        top: 0;
        left: 0;

        li {
          margin: 0 auto;
          .link {
            color: #ffffff;
          }
        }
      }
    }
  }

</style>
