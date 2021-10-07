<template>
  <div>
    <!-- Grupo de elementos #1 -->
    <div class="contenedor-header">
      <!-- Contenedor logo -->
      <div class="contenedor-header__logo">
        <img src="../assets/images/logo-minimal.png" alt="Logo Bibliotech" />
      </div>

      <!-- Contenedor de usuario actual -->
      <div class="contenedor-header__usuario">
        <div class="header__usuario">
          <!-- Nombre de usuario actual -->
          <p class="usuario_titulo">Nombre de usuario</p>

          <!-- Tipo de usuario actual -->
          <div class="header__usuario-label">
            <div class="header__usuario-label-texto">root</div>
          </div>
        </div>
      </div>
    </div>
    <!-- FIN Grupo de elementos #1 -->

    <!-- Grupo de elementos #2 -->
    <div class="contenedor-body-1">
      <!-- Primer elemento de la barra lateral -->
      <div class="contenedor-barra-1" onclick="javascript:enlaceRecientes();">
        <div class="elemento-1">
          <div class="elemento-1__icono">
            <span class="material-icons material-icons--settings">restore</span>
          </div>
          <p class="elemento-1__titulo ">Recientes</p>
        </div>
      </div>

      <!-- Segundo elemento de la barra lateral -->
      <div
        class="contenedor-barra-2 contenedor-barra-1--actual"
        onclick="javascript:enlaceArticulos();"
      >
        <div class="elemento-1">
          <div class="elemento-1__icono">
            <span class="material-icons material-icons--settings-actual"
              >import_contacts</span
            >
          </div>
          <p class="elemento-1__titulo elemento-1__titulo--actual">Artículos</p>
        </div>
      </div>

      <!-- Tercer elemento de la barra lateral -->
      <div
        class="contenedor-barra-3"
        onclick="javascript:enlaceAdministradores();"
      >
        <div class="elemento-1">
          <div class="elemento-1__icono">
            <span class="material-icons material-icons--settings">group</span>
          </div>
          <p class="elemento-1__titulo">Administradores</p>
        </div>
      </div>
    </div>
    <!-- FIN Grupo de elementos #2 -->

    <!-- Grupo de elementos #3 -->
    <div class="contenedor-body-2">
      <!-- Tercer elemento de la barra lateral -->
      <div class="contenedor-barra-1" onclick="javascript:enlaceSalir();">
        <div class="elemento-1">
          <div class="elemento-1__icono">
            <span class="material-icons material-icons--settings">logout</span>
          </div>
          <p class="elemento-1__titulo">Salir</p>
        </div>
      </div>
    </div>
    <!-- FIN Grupo de elementos #3 -->
  </div>
</template>

<style scoped>
/* Espacio para el logo y el nombre */
.contenedor-header {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;

  width: 100%;
  height: 9vw;
  border-bottom: 1px solid #0000001f;
}

.contenedor-header__logo {
  /* background-color: rgba(0, 255, 200, 0.082); WIREFRAME*/

  width: 100%;
  height: 100%;
  /* padding: 0.625rem; */
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  padding-top: 1.25rem;

  box-sizing: border-box;
}

.contenedor-header__logo img {
  width: 100%;
}

.contenedor-header__usuario {
  /* background-color: crimson; WIREFRAME*/

  display: flex;
  flex-direction: column;
  justify-content: space-evenly;

  width: 100%;
  height: 2.5rem;

  padding-left: 0.625rem;
  padding-right: 0.625rem;

  box-sizing: border-box;
}

.header__usuario {
  /* background-color: rgb(255, 0, 242); WIREFRAME*/

  padding: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 1.25rem;
}

.usuario_titulo {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
}

.header__usuario-label {
  background-color: #ffaa00 !important;

  display: inline-flex;

  padding-left: 0.625rem;
  padding-right: 0.625rem;

  border-radius: 6px;
}

.header__usuario-label-texto {
  font-family: "Roboto", sans-serif;
}

/* Primer cuerpo del menú */
.contenedor-body-1 {
  /* background-color: rgba(0, 0, 0, 0.082); WIREFRAME*/

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

/* Primera Sección */
.contenedor-barra-1 {
  /* background-color: crimson;  WIREFRAME*/

  display: flex;
  flex-direction: column;
  justify-content: space-evenly;

  width: 100%;
  height: 2.5rem;

  padding-left: 0.625rem;
  padding-right: 0.625rem;

  box-sizing: border-box;

  /*border-radius: 4px;*/
}

/* Primera Sección - elemento*/
.elemento-1 {
  /* background-color: rgb(255, 0, 242); WIREFRAME*/

  padding: 0;
  display: flex;
  align-items: center;
  width: 100%;
  height: 1.25rem;
}

/* Primera Sección - icono*/
.elemento-1__icono {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;

  margin-right: 1.5rem;
}

.elemento-1__titulo {
  color: #828282;
  font-family: "Roboto", sans-serif;
  font-size: 1.1rem;
  font-weight: 300;
  letter-spacing: 0.2px;
}

/* Borde gris al pasar el mouse por encima del menú*/
.contenedor-barra-1:hover {
  background-color: #00000009;
  border-radius: 4px;
  cursor: pointer;
}

.contenedor-barra-2:hover {
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

.contenedor-barra-2 {
  /* background-color: yellowgreen;  WIREFRAME*/

  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  width: 100%;
  height: 2.5rem;

  padding-left: 0.625rem;
  padding-right: 0.625rem;

  box-sizing: border-box;

  /*border-radius: 4px;*/
}

.contenedor-barra-3 {
  /* background-color: burlywood;  WIREFRAME*/

  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  width: 100%;
  height: 2.5rem;

  padding-left: 0.625rem;
  padding-right: 0.625rem;

  box-sizing: border-box;

  /*border-radius: 4px;*/
}

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
