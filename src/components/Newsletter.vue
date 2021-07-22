<template>
  <div class="new">
    <section class="new-container">
      <h2>¡Unete a las novedades y promociones!</h2>
      <form>
        <input type="text" placeholder="Ingresa tu nombre" />
        <input type="email" placeholder="Ingresa tu mail" />
        <Button color="primary" size="base">Suscribirme</Button>
      </form>
    </section>
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Newsletter",
  components: { Button },
  data() {},
};
</script>

<style scoped>
    .new{
        display: flex;
        padding: 1rem;
        background-color: #F2F2F2;
        justify-content: center;
        text-align: center;
    }
    form{
        display:flex;
        flex-direction: column;
        gap:1rem;
    }
    form>input{
        padding: .75rem 1rem;
        border-radius: 4px;
        background-color: #fff;
        border: none;
    }
    @media screen and (min-width: 780px) {
        form {
            flex-direction: row;
        }
    }
</style>
