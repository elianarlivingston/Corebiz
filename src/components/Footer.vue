<template>
  <footer class="footer">
    <div class="footer__container">
      <article class="footer__contact">
        <h2>Ubicacion</h2>
        <p>
          <span>Avenida Andromeda, 2000. Bloco 6 e 8</span>
          <span>Alphaville SP</span>
          <span>brasil@corebiz.ag</span>
          <span>+55 11 3090 1039</span>
        </p>
      </article>

      <div class="footer__buttons">
        <button>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-envelope-fill"
            viewBox="0 0 16 16"
          >
            <path
              d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555zM0 4.697v7.104l5.803-3.558L0 4.697zM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757zm3.436-.586L16 11.801V4.697l-5.803 3.546z"
            />
          </svg>
          <span>CONTACTANOS</span>
        </button>
        <button>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-headset"
            viewBox="0 0 16 16"
          >
            <path
              d="M8 1a5 5 0 0 0-5 5v1h1a1 1 0 0 1 1 1v3a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V6a6 6 0 1 1 12 0v6a2.5 2.5 0 0 1-2.5 2.5H9.366a1 1 0 0 1-.866.5h-1a1 1 0 1 1 0-2h1a1 1 0 0 1 .866.5H11.5A1.5 1.5 0 0 0 13 12h-1a1 1 0 0 1-1-1V8a1 1 0 0 1 1-1h1V6a5 5 0 0 0-5-5z"
            />
          </svg>
          <span>HABLA CON UN CONSULTOR</span>
        </button>
      </div>

      <div class="footer__partners">
        <figure>
          <img src="../assets/logo-corebiz-white.svg" alt="" />
        </figure>
        <figure>
          <img src="../assets/logo-vtex.png" alt="" />
        </figure>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  setup() {
    return {};
  },
};
</script>

<style scoped>
.footer {
  width: 100%;
  padding: 1rem;
  color: white;
  background-color: black;
}
.footer__container {
  max-width: 900px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.footer__contact > p {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  font-size: 1rem;
}
.footer__contact h2::after {
  content: "";
  display: flex;
  width: 40px;
  height: 3px;
  background-color: white;
  margin-top: 0.5rem;
}

.footer__buttons {
  
}
</style>
