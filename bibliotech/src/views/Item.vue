<template>
  <div class="d-flex">


    <!-- Barra de navegación -->
    <aside class="d-flex flex-column barra-lateral">
      <SideBar :option="2"/>
    </aside> <!-- FIN Barra de navegación -->


    <!-- Contenido principal de la pagina -->
    <main class="contenido">

      <!-- Parte superior (Migas de pan y botones) -->
      <div class="barra-superior">

        <div class="contenedor-superior">
          
            <!-- Migas de pan -->
            <div class="contenedor-migasdepan">
              <MigaMain />
            </div> <!-- FIN Migas de pan -->
            
            <!-- Botones con funciones -->
            <div class="contenedor-botonessuperiores">
              <!-- Boton para crear elementos -->
              <div class="boton__crear" onclick="javascript:enlaceNuevoArticulo()">
                <div class="icono-superior">
                    <span class="mb-0 material-icons material-icons--boton-sup">add</span>
                </div>
              </div> <!-- FIN Boton para crear elementos -->
            </div> <!-- FIN Botones con funciones -->

        </div>

      </div> <!-- FIN Parte superior (Migas de pan y botones) -->

      <!-- Contenido luego de las migas de pan (Cartas) -->
      <div class="seccion-central">
        <!-- Grilla dinamica -->
        <div class="grilla-responsive">
          <Tarjeta v-for="item, index in items" :key="index" :index="index" :item="item"/>
        </div> <!-- FIN Grilla dinamica -->
      </div> <!-- FIN Contenido luego de las migas de pan (Cartas) -->

    </main> <!-- FIN Contenido principal de la pagina -->
  </div>
</template>
<script>
import SideBar from "../components/SideBar.vue"
import Tarjeta from "../components/Card.vue"
import Miga from "../components/BreadCrumbsLinks.vue"
import MigaMain from "../components/BreadCrumbsMain.vue"

export default {
  components: {
    SideBar,
    Tarjeta,
    Miga,
    MigaMain
  },
  data() {
    return {
      items: [
        { book_title: 'Science & Technology', book_author: 'Ravi Agrahari', image:'placeholder.png'},
        { book_title: 'Introducing Go', book_author: 'Caleb Doxsey', image:'placeholder.png'},
        { book_title: 'Programa o serás programado', book_author: 'Douglas Rushkoff', image:'placeholder.png'},
        { book_title: 'New Yorker Issue Vol 85-26', book_author: 'The New Yorker', image:'placeholder.png'},
        
        
      ]
    }
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
.contenedor-botonessuperiores {
    display: flex;
    flex-direction: row;
    align-items: center;
    height: 100%;
}
.boton__crear {
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: #ff6c38;
    width: 2.375rem;
    height: 2.375rem;
    border-radius: 4px;
    box-sizing: border-box;
    margin-right: 1.25rem;
    cursor: pointer;
}
.boton__crear:hover {
    background-color: #db5f32;
}
.icono-superior {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-content: center;
}
.material-icons--boton-sup {
    color: #FFFFFF;
    font-size: 2.375rem;
}
.material-icons--boton-sup-fixed {
    color: #FFFFFF;
    font-size: 1.7rem;
}
.boton__seleccionar {
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: #485EB2;
    width: 2.375rem;
    height: 2.375rem;
    border-radius: 4px;
    box-sizing: border-box;
    margin-right: 1.25rem;
}
.boton__borrar {
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: #C30000;
    width: 2.375rem;
    height: 2.375rem;
    border-radius: 4px;
    box-sizing: border-box;
    margin-right: 1.25rem;
}
.boton__editar {
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: #485EB2;
    width: 2.375rem;
    height: 2.375rem;
    border-radius: 4px;
    box-sizing: border-box;
    margin-right: 1.25rem;
    padding: 6px;
    cursor: pointer;
}
.boton__editar:hover {
    background-color: #3a4b8d;
} /* FIN Botones superiores */
/* Migas de pan */
.migas__principal--texto {
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
    font-size: 2.125rem;
    letter-spacing: 0.016rem;
}
.migas__principal--texto a {
    text-decoration: none;
    color: #AAAAAA
}
.miga1 {
    color: #AAAAAA;
}
.separador {
    color: #AAAAAA;
    padding-left: 2rem;
    padding-right: 2rem;
}
/* FIN migas de pan */

.seccion-central {
    width: 100%;
    height: 100%;
    padding-left: 5rem;
    padding-right: 5rem;
    box-sizing: border-box;
}
.grilla-responsive {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 0.46fr));
    grid-template-rows: repeat(1, 300px);
    grid-gap: 1rem;
    grid-auto-flow: dense;
    justify-items: center;
    overflow: hidden;
    box-sizing: border-box;
    padding-bottom: 40px;
}
</style>
