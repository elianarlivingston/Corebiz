<template>
  <Header></Header>
  <Newsletter></Newsletter>
  <Footer></Footer>
</template>
<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Newsletter from "./components/Newsletter.vue";

export default {
  name: "App",
  components: { Header, Footer, Newsletter },
};
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
</style>
