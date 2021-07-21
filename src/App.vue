<template>
  <Header></Header>
  <!-- <Footer></Footer> -->
  <Button color="primary" size="sm"> Hola! </Button>
  <Button color="secondary"> Hola! </Button>
  <Button size="lg"> Hola! </Button>
</template>
<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Button from "./components/Button.vue";

export default {
  name: "App",
  components: { Header, Footer, Button },
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
