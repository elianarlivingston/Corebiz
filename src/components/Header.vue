<template>
  <header class="header">
    <nav class="header__container">
      <!-- boton de menu -->
      <button class="header__menu">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          fill="currentColor"
          class="bi bi-list"
          viewBox="0 0 16 16"
        >
          <path
            fill-rule="evenodd"
            d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"
          />
        </svg>
      </button>

      <!-- logo -->
      <figure class="header__logo">
        <img src="../assets/logo-corebiz.svg" alt="" />
      </figure>

      <!-- my account -->
      <button class="header__myaccount">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="currentColor"
          class="bi bi-person"
          viewBox="0 0 16 16"
        >
          <path
            d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0zm4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4zm-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10c-2.29 0-3.516.68-4.168 1.332-.678.678-.83 1.418-.832 1.664h10z"
          />
        </svg>
        <span>Mi cuenta</span>
      </button>

      <!-- carrito -->
      <div class="header__cart">
        <button>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            fill="currentColor"
            class="bi bi-cart4"
            viewBox="0 0 16 16"
          >
            <path
              d="M0 2.5A.5.5 0 0 1 .5 2H2a.5.5 0 0 1 .485.379L2.89 4H14.5a.5.5 0 0 1 .485.621l-1.5 6A.5.5 0 0 1 13 11H4a.5.5 0 0 1-.485-.379L1.61 3H.5a.5.5 0 0 1-.5-.5zM3.14 5l.5 2H5V5H3.14zM6 5v2h2V5H6zm3 0v2h2V5H9zm3 0v2h1.36l.5-2H12zm1.11 3H12v2h.61l.5-2zM11 8H9v2h2V8zM8 8H6v2h2V8zM5 8H3.89l.5 2H5V8zm0 5a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0zm9-1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0z"
            />
          </svg>
        </button>

        <span class="header__badge">1</span>
      </div>

      <!-- search -->
      <div class="header__search">
        <input type="text" placeholder="¿Qué estás buscando?" />
        <img src="../assets/search.svg" alt="" />
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  setup() {},
};
</script>

<style scoped>
.header {
  width: 100%;
  padding: 1rem;
}

.header__container {
  max-width: 900px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, auto);
  grid-template-areas: "menu logo cart" "search search search";
  align-items: center;
}

.header__menu {
  grid-area: menu;
  justify-self: start;
  border: none;
  background: transparent;
}

.header__logo {
  grid-area: logo;
  margin: 0;
  padding: 0;
  width: 150px;
}

.header__logo > img {
  display: block;
  width: 100%;
}

.header__myaccount {
  display: none;
  border: none;
  background: transparent;
}

.header__cart {
  grid-area: cart;
  justify-self: end;
  display: flex;
}

.header__cart button {
  border: none;
  background: transparent;
}

.header__badge {
  /* 1rem es 16px */
  width: 1.25rem;
  height: 1.25rem;
  font-size: 0.85rem;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: tomato;
  color: white;
  align-self: flex-start;
}

.header__search {
  padding: 0.25rem; /*4px */
  grid-area: search;
  display: flex;
  align-items: center;
  border-bottom: 2px solid #212121;
}

.header__search input {
  padding: 0.25rem; /*4px */
  border: none;
  background: transparent;
  outline: none;
  flex-grow: 1;
}

.header__search img {
  width: 20px;
  height: 20px;
}

/* max-width: hasta este tamalo hace esto */
/* min-width: despues de este tamaño hace esto */

/* Para Desktop */
@media screen and (min-width: 780px) {
  .header__container {
    grid-template-columns: auto 1fr auto auto;
    grid-template-rows: auto;
    gap: 2rem;
    grid-template-areas: "logo search myaccount cart";
  }

  .header__menu {
    display: none;
    border: none;
    background: transparent;
  }

  .header__myaccount {
    display: flex;
    align-items: center;
    gap: 1rem;
    grid-area: myaccount;
  }
}
</style>
