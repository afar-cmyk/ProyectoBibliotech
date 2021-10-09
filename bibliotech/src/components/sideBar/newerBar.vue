<template>
  <!-- Primer elemento de la barra lateral -->
  <div class="contenedor-barra-1" onclick="javascript:enlaceRecientes();">
    <div class="elemento-1">
      <div class="elemento-1__icono">
        <span class="material-icons material-icons--settings">restore</span>
      </div>
      <p class="elemento-1__titulo mb-0">Recientes</p>
    </div>
  </div>
</template>

<style scoped>
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
</style>
