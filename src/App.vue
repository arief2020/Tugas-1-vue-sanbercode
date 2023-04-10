<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h1>Hello Vue</h1>
  <h3>Nama : Muhammad Syaifullah Al Arief</h3>
  <h3>Kelas: Bootcamp Karyawan Batch 44</h3>
  <Navbar 
  :pages="pages"
  :active-page="activePage"
  :nav-link-click="(index) => activePage = index"
  ></Navbar>
  <PageViewer
  :page="pages[activePage]"
  ></PageViewer>
</template>

<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';

export default {
  components: {
    PageViewer,
    Navbar
  },
  data() {
    return {
      activePage: 0,
      pages: [
        {
          link: {text: 'Home', url: 'index.html'},
          pageTitle: 'Home Page',
          content: 'This is the Home Content'
        },
        {
          link: {text: 'About', url: 'about.html'},
          pageTitle: 'About Page',
          content: 'This is the About Content'
        },
        {
          link: {text: 'Contact', url: 'contact.html'},
          pageTitle: 'Contact Page',
          content: 'This is the Contact Content'
        },
      ]
    }
  },
  components: {
    Navbar,
    PageViewer
}
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
