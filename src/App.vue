<template>
  <HeaderComponentVue />

  <router-view />

  <FooterComponent />
  
</template>

<script>
import FooterComponent from '@/components/footer/FooterComponent.vue';
import HeaderComponentVue from './components/header/HeaderComponent.vue';

export default {
  components: {
    FooterComponent,
    HeaderComponentVue
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>




