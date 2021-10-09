<template>
  <div>
    <!-- Grupo de elementos #1 -->
    <div class="d-flex flex-column justify-content-around contenedor-header">
      <!-- Contenedor logo -->
      <div class="contenedor-header__logo">
        <img src="../assets/images/logo-minimal.png" alt="Logo Bibliotech" />
      </div>

      <!-- Contenedor de usuario actual -->
      <div
        class="d-flex flex-column justify-content-around contenedor-header__usuario"
      >
        <div
          class="d-flex justify-content-between align-items-center header__usuario"
        >
          <!-- Nombre de usuario actual -->
          <p class="d-flex usuario_titulo mb-0">
            Nombre de usuario
          </p>

          <!-- Tipo de usuario actual -->
          <labelRoot />
          <!-- FIN Tipo de usuario actual -->
        </div>
      </div>
    </div>
    <!-- FIN Grupo de elementos #1 -->

    <!-- Grupo de elementos #2 -->
    <div class=" contenedor-body-1">
      <newerBar />

      <itemBar />

      <adminBar />

    </div>
    <!-- FIN Grupo de elementos #2 -->

    <!-- Grupo de elementos #3 -->
    <div class="contenedor-body-2">
      <logoutBar />
    </div>
    <!-- FIN Grupo de elementos #3 -->
  </div>
</template>

<script>
// Labels //
import labelRoot from "../components/labelRoot.vue"
import labelAdmin from "../components/labelAdmin.vue"
// Elementos de la barra de navegación //
import newerBar from "../components/sideBar/newerBar.vue"
import itemBar from "../components/sideBar/itemBar.vue"
import adminBar from "../components/sideBar/adminBar.vue"
import logoutBar from "../components/sideBar/logoutBar.vue"

export default {
  components: {
    labelRoot,
    labelAdmin,
    newerBar,
    itemBar,
    adminBar,
    logoutBar
  },
};
</script>

<style scoped>
/* Espacio para el logo y el nombre */
.contenedor-header {
  width: 100%;
  height: 9vw;
  border-bottom: 1px solid #0000001f;
}

.contenedor-header__logo {
  width: 100%;
  height: 100%;
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  padding-top: 1.25rem;
  box-sizing: border-box;
}

.contenedor-header__logo img {
  width: 100%;
}

.contenedor-header__usuario {
  width: 100%;
  height: 2.5rem;
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  box-sizing: border-box;
}

.header__usuario {
  padding: 0;
  width: 100%;
  height: 1.25rem;
}

.usuario_titulo {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  margin-bottom: 0;
}

/* Primer cuerpo del menú */
.contenedor-body-1 {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;

  width: 100%;
  height: 10rem;

  padding-left: 0.625rem;
  padding-right: 0.625rem;

  border-bottom: 1px solid #0000001f;

  box-sizing: border-box;
}

/* Borde gris al pasar el mouse por encima del menú*/
.contenedor-barra-1:hover {
  background-color: #00000009;
  border-radius: 4px;
  cursor: pointer;
}



.contenedor-barra-3:hover {
  background-color: #00000009;
  border-radius: 4px;
  cursor: pointer;
}

/* <-----------------------------------> */

/* Seleccion actual en la barra de menú */
.contenedor-barra-1--actual {
  background-color: #ffe6e0 !important;
  border-radius: 4px;
}

.elemento-1__titulo--actual {
  color: #ff3000;
  font-weight: 400;
}

.material-icons--settings-actual {
  color: #ff3000;
}

/* <-----------------------------------> */


/* Segunda sección del menú */

.contenedor-body-2 {
  /* background-color: rgba(8, 43, 243, 0.082); WIREFRAME*/

  display: flex;
  flex-direction: column;

  width: 100%;
  height: 3.75rem;

  padding-top: 0.625rem;
  padding-left: 0.625rem;
  padding-right: 0.625rem;

  box-sizing: border-box;
}
</style>
