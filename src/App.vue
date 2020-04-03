<template>
  <div id="app">
    <div class="h-screen w-screen overflow-auto bg-gradient-tl-cyan-blue">

      <Header />

      <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/equipment">Equipment</router-link> |
        <router-link to="/qualifications">Qualifications</router-link> |
        <router-link to="/about">About</router-link>
      </div>



      <router-view />

      <Contact />
    </div>
  </div>
</template>

<script>
  import Header from '@/components/Header.vue'
  import Contact from '@/components/Contact.vue'

  export default {
    components: {
      Header,
      Contact
    },
    data() {
      return {
        image: "@/assets/img/pexels-2.jpeg"
      };
    },
  }

</script>

<style>
#backgroundImg {
  background-size: cover;
  z-index: -100;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 10px;
  text-align: center;
  font-size: 1.5em;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
