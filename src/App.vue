<script>
import Nav from './components/Nav.vue';
import Home from './components/Home.vue';
import Footer from './components/Footer.vue';
import Book from './components/Book.vue';
import Pay from './components/Pay.vue';
export default {
  components: {
    Nav,
    Home,
    Footer,
    Book,
    Pay
  }, data() {
    return {
      currentPage: 'home'
    }
  },
  methods: {
    changePage(page) {
      this.currentPage = page
    }
  }
}
</script>

<template>
  <Nav @goToPage="changePage" />
  <Home v-if="currentPage === 'home'" />
  <Footer />
  <Book v-if="currentPage === 'book'" />
  <Pay v-if="currentPage === 'Pay'" />
</template>
