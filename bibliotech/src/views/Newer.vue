<template>
  <div class="d-flex">
    <!-- Barra de navegación -->
    <aside class="d-flex flex-column barra-lateral">
      <SideBar />
    </aside> <!-- FIN Barra de navegación -->
    <main class="contenido">
      <div class="seccion-central">
        <div class="segmentos-centrales">

          <!-- Contenedor rectangular que contiene a el titulo y a las tarjetas -->
          <div class="segmentos-centrales__contenedor">

            <!-- Titulo -->
            <div class="caja__titulo">
              <p class="mb-0 caja__titulo--estilos">Articulos Recientes</p>
            </div> <!-- FIN Titulo -->

            <!-- Envoltura para las cajas -->
            <div class="caja__cartas">
              <Tarjeta />
              <Tarjeta />
              <Tarjeta />
              <Tarjeta />
            </div> <!-- FIN Envoltura para las cajas -->

          </div>

              <!-- Separador central -->
              <div class="segmentos-centrales__separador">
                <div class="separador__caja"></div>
              </div> <!-- FIN Separador central -->

              <!-- Contenedor rectangular que contiene a el titulo y a las tarjetas -->
          <div class="segmentos-centrales__contenedor">

            <!-- Titulo -->
            <div class="caja__titulo">
              <p class="mb-0 caja__titulo--estilos">Administradores Recientes</p>
            </div> <!-- FIN Titulo -->

            <!-- Envoltura para las cajas -->
            <div class="caja__cartas">
              <Tarjeta />
              <Tarjeta />
              <Tarjeta />
              <Tarjeta />
            </div> <!-- FIN Envoltura para las cajas -->

          </div>

        </div>
      </div>
    </main>
  </div>
</template>
<script>
import SideBar from "../components/SideBar.vue"
import Tarjeta from "../components/TarjetaArticulos.vue"

export default {
  components: {
    SideBar,
    Tarjeta
  },
};
</script>
<style scoped>
.barra-lateral {
  background-color: white;
  width: 16vw;
  height: 100vh;
  border-right: 1px solid #0000001f;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.082), 0 1px 2px rgba(0, 0, 0, 0.158);
}
.contenido {
    display: flex;
    flex-direction: column;
    align-items: center;
    align-content: space-around;
    width: 84vw;
    height: 100vh;
}
.seccion-central {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 100vh;
    padding: 5rem;
    box-sizing: border-box;
}
.segmentos-centrales {
    height: 100%;
    width: 100%;
    overflow: hidden;
    box-sizing: border-box;
}
.segmentos-centrales__contenedor {
    padding-left: 1px;
    display: flex;
    flex-direction: column;
    padding-bottom: 2px;
}
.caja__titulo {
    display: flex;
    flex-direction: row;
    align-items: center;
    height: 60px;
}
.caja__titulo--estilos {
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
    font-size: 1.5rem;
    letter-spacing: 0.016rem;
}
.caja__cartas {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: flex-start;
}
.segmentos-centrales__separador {
    background-color: #0000001F;
    margin-top: 39px;
    margin-bottom: 20px;
}
.separador__caja {
    height: 1px;
    width: 100%;
}
</style>
