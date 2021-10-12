<template>
  <div class="d-flex">

    <aside class="d-flex flex-column barra-lateral">
      <SideBar />
    </aside>

    <!-- Contenido principal de la pagina -->
    <main class="contenido">

      <!-- Parte superior (Migas de pan y botones) -->
      <div class="barra-superior">

        <div class="contenedor-superior">

            <!-- Migas de pan -->
            <div class="contenedor-migasdepan">
              <MigasLinks />
            </div> <!-- FIN Migas de pan -->
        </div>

      </div> <!-- FIN Parte superior (Migas de pan y botones) -->



      <!-- Contenido luego de las migas de pan (Cartas) -->
      <div class="seccion-central d-flex justify-content-center">
          <NewItem />
      </div> <!-- FIN Contenido luego de las migas de pan (Cartas) -->

    </main> <!-- FIN Contenido principal de la pagina -->

  </div>
</template>
<script>
import SideBar from  "../components/SideBar.vue"
import MigasLinks from "../components/BreadCrumbsLinks.vue"
import NewItem from "../components/contentManagers/NewItem.vue"

export default {
  components: {
    SideBar,
    MigasLinks,
    NewItem
  }
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
.barra-superior {
    display: flex;
    justify-content: center;
    height: 6.25rem !important;
    width: 100%;
    padding-top: 40px !important;
    padding-bottom: 40px !important;
    margin-top: 20px;
}
.contenedor-superior {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 100%;
    height: 100%;
    padding-left: 3.75rem;
}
.contenedor-migasdepan {
    display: flex;
    flex-direction: row;
    align-items: center;

    height: 100%;
}
.seccion-central {
    width: 100%;
    height: 100vh;
    padding-left: 5rem;
    padding-right: 5rem;
    box-sizing: border-box;
}
</style>
