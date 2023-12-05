<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';
export default {
  data() {
    return {
      menu: [
        "Home",
        "Recipes",
        "Places",
        "Blog",
        "About",
        "Contact",      
      ],
      social: [
      "fa-brands fa-facebook-f",
      "fa-brands fa-instagram",
      "fa-brands fa-twitter",
      "fa-brands fa-youtube",
      ],
    }
  },
  components: {
    AppHeader,
    AppFooter,
    AppMain,
  }
}

</script>

<template>

<AppHeader :menu="menu" :social="social"/>
<AppMain />
<AppFooter :menu="menu" :social="social"/>
  
</template>

<style lang="scss">
@import "@fortawesome/fontawesome-free/css/all.css";
.my_container {
  margin: 0 auto;
  width: 70%;
}
</style>