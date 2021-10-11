<template>
  <div class="carta">
      <!-- Seccion superior de la carta -->
      <div class="carta-header">
          <div class="carta-header__texto">
              <p class="carta-header__texto carta-header__texto--titulo">{{ item.book_title }}</p>
              <p class="carta-header__texto carta-header__texto--subtitulo">{{ item.book_author }}</p>
          </div>
      </div>
      <!-- Seccion central de la carta -->
      <div class="carta-body">
          <div class="carta-body__imagen">
              <!-- <img src="../assets/images/placeholder.png"> -->
              <img :src="`cardImage/${item.image}`" alt="">
          </div>
      </div>
      <!-- Seccion inferior de la carta -->
      <div class="carta-footer">
          <div class="carta-footer__botones">
              <a class="carta-footer__botones carta-footer__botones--cancelar"
                href="">Borrar</a>
              <input class="carta-footer__botones carta-footer__botones--boton" type="submit"
                value="EDITAR" >
          </div>
      </div>
  </div>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      default: () => {}
    },
  }
}
</script>
<style scoped>
.carta {
  background-color: #ffffff;
  display: flex;
  flex-direction: column;
  width: 316px;
  height: 280px;
  border-radius: 7px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  box-sizing: border-box;
  margin-top: 2px;
}
.carta-header {
  height: 68px;
  width: 100%;
  display: flex;
  align-items: center;
}
.carta-header__texto {
  height: 42px;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 1rem;
  box-sizing: border-box;
}
.carta-header__texto--titulo {
  font-family: "Roboto";
  font-size: 1rem;
  font-weight: 500;
  padding: 0%;
  margin: 0%;
}
.carta-header__texto--subtitulo {
  font-family: "Roboto";
  font-size: 0.75rem;
  font-weight: 300;
  padding: 0%;
  margin: 0%;
}
.carta-body {
  background-color: #E6E6E6;

  height: 178px;
  display: flex;
  justify-content: center;
}
.carta-body__imagen {
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow: hidden;
  max-height: 174px;
  max-width: 316px;
  box-sizing: border-box;
}
.carta-body img {
  max-width: 100%;
  height: auto;
  width: 316px;
}
.carta-footer {
  height: 40px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
}
.carta-footer__botones {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.carta-footer__botones--cancelar {
  font-family: 'Roboto', sans-serif;
  color: #FF6C38;
  font-size: 0.80rem;
  text-decoration: none;
}
.carta-footer__botones--cancelar:hover {
  color: #da5e31;
}
.carta-footer__botones--boton {
  font-family: 'Roboto', sans-serif;
  border-radius: 4px;
  font-size: 0.625rem;
  font-weight: 500;
  color: #FFFFFF;
  background-color: #485EB2;
  margin-left: 7px;
  padding: 6px;
  border: none;
  outline: none;
  cursor: pointer;
}
.carta-footer__botones--boton:hover {
  background-color: #3f529c;
}
</style>
