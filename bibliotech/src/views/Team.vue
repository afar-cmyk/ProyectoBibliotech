 <template>
  <div>
    <NavBar />
     <main class="main-section">
       <!--Inicio de contenido de la página team-->
       <div class="line-container">
        <h1>Equipo</h1>
        <h3>Conozca a nuestro equipo</h3>
      </div>
      <!--Inicio contenido información de las personas del equipo-->
      <b-container fluid>
        <b-row class="row-team">
          <b-col cols="12" md="6" lg="4">
            <b-card>
              <div class="team-one">
                <b-img :src="require('../assets/images/andres.png')" />
                <b-text>
                  <h4 class="name">Andrés Felipe Álvarez</h4>
                  <p class="info">Tecnólogo en producción de Multimedia, apasionado por la fotografía y el diseño</p>
                  <h5 class="occupation">Desarrollador backend y frontend, diseñador web</h5>
                  <b-button href="https://github.com/afar-cmyk" target="_blank" class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="6" lg="4">
             <b-card>
              <div class="team-two">
                <b-img :src="require('../assets/images/john.jpg')" />
                <b-text>
                  <h4 class="name">John Stiven Vásquez</h4>
                  <p class="info">Estudiante universitario interesado en la programación y con experiencia en Java</p>
                  <h5 class="occupation">Desarrollador backend, bases de datos</h5>
                  <b-button href="https://github.com/jsstiven" target="_blank" class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="6" lg="4">
             <b-card>
              <div class="team-three">
                <b-img :src="require('../assets/images/kelly.jpg')" />
                <b-text>
                  <h4 class="name">Kelly Monroy Carrillo</h4>
                  <p class="info">Diseñadora digital y multimedia, ilustradora y artista, en aprendizaje del mundo del desarrollo</p>
                  <h5 class="occupation">Diseñadora web y desarrolladora frontend</h5>
                  <b-button href="https://github.com/muakarada" target="_blank" class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="6" lg="4">
             <b-card>
              <div class="team-four">
                <b-img :src="require('../assets/images/luis.jpg')" />
                <b-text>
                  <h4 class="name">Luis Fernando Delgado</h4>
                  <p class="info">Administrador de empresas, interesado por el aprendizaje en tecnología y desarrollo</p>
                  <h5 class="occupation">Desarrollador backend y web</h5>
                  <b-button href="https://github.com/lufermaxi" target="_blank" class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
          <b-col cols="12" md="6" lg="4">
             <b-card>
              <div class="team-five">
                <b-img :src="require('../assets/images/ex-photo-man.jpg')" />
                <b-text>
                  <h4 class="name">Juan Esteban Castiblanco</h4>
                  <p class="info">Estudiante de economía e Ingeniería estadística, estudiante de Misión TIC</p>
                  <h5 class="occupation">Desarrollador backend</h5>
                  <b-button href="https://github.com/Jesteban247" target="_blank" class="contact-team">Contacto</b-button>
                </b-text>
              </div>
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    <!--Fin contenido del equipo-->
    </main>
    <Footer />
  </div>
</template>
<script>
import NavBar from '../components/navbar.vue'
import Footer from '../components/footer.vue'

export default {
  components: {
    NavBar,
    Footer,
  },
};
</script>
<style>
.btn-secondary{
    background-color: #485eb2 !important;
    border: 1px solid #485eb2 !important;
}
.card{
    border-color: #ff3000 !important;
    margin-bottom: 0.8rem;
    display: flex;
    flex-direction: column;
}
</style>
