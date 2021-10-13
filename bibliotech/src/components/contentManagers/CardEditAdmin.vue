<template>
  <div class="carta">
      <!-- Seccion superior de la carta -->
      <div class="carta-header">
          <div class="carta-header__texto">
              <p class="carta-header__texto carta-header__texto--titulo">{{ admin.name }}</p>
              <p class="carta-header__texto carta-header__texto--subtitulo">{{ admin.username }}</p>
          </div>
      </div>
      <!-- Seccion central de la carta -->
      <div class="carta-body">
          <div class="carta-body__imagen">
              <!-- <img src="../assets/images/placeholder.png"> -->
              <img src="../../assets/images/placeholder.png" alt="">
          </div>
      </div>
      <!-- Seccion inferior de la carta -->
      <div class="carta-footer">
        <div class="carta-footer__botones">
          <a class="carta-footer__botones carta-footer__botones--cancelar"
            href="">Borrar</a>
          <div>

            <b-button v-b-modal="`modal-${index}`" @click="editAdmin()"  class="carta-footer__botones carta-footer__botones--boton">Editar</b-button>
            <b-modal class="titulo-modal" :id="`modal-${index}`" :title="`Editando: ${form.name} ${form.lastname}`" hide-footer>
              <b-form @submit="onSubmit">
                <b-container>
                  <b-row>
                    <b-col>
                      <div class="form-floating mt-4 mb-4">
                        <input v-model="form.username" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                        <label label for="mb-0 floatingInput" class="text-secondary">Nombre de usuario</label>
                      </div>
                    </b-col>
                  </b-row>
                  <b-row>
                    <b-col>
                      <div class="form-floating mb-4">
                        <input v-model="form.password" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                        <label label for="mb-0 floatingInput" class="text-secondary">Contraseña</label>
                      </div>
                    </b-col>
                  </b-row>
                  <b-row>
                    <b-col>
                      <div class="form-floating mb-4">
                        <input v-model="form.email" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                        <label label for="mb-0 floatingInput" class="text-secondary">Email</label>
                      </div>
                    </b-col>
                  </b-row>
                  <b-row>
                    <b-col>
                      <div class="form-floating mb-4">
                        <input v-model="form.name" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                        <label label for="mb-0 floatingInput" class="mb-0 text-secondary">Nombre</label>
                      </div>
                    </b-col>
                  </b-row>
                  <b-row>
                    <b-col>
                      <div class="form-floating">
                        <input v-model="form.lastname" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                        <label label for="mb-0 floatingInput" class="mb-0 text-secondary">Apellido</label>
                      </div>
                    </b-col>
                  </b-row>
                </b-container>
              <div class="mt-4 text-center">
                <b-button class="boton-modal-b mb-0" variant="danger" @click="$bvModal.hide(`modal-${index}`)">Volver</b-button>
                <b-button type="submit" variant="success" class="boton-modal-a mb-0">Crear</b-button>
              </div>
              </b-form>
            </b-modal>
          </div>
        </div>
      </div>
  </div>
</template>
<script>
export default {
  props: {
    admin: {
      type: Object,
      default: () => {}
    },
    index: {
      type:Number,
      default: () => 1
    }
  },
  data() {
    return {
      form: {
        username: '',
        password: '',
        email: '',
        name: '',
        lastname: ''
      }
    }
  },
  methods: {
    editAdmin() {
      console.log(this.admin)
      this.form.username = this.admin.username,
      this.form.password = this.admin.password,
      this.form.email = this.admin.email,
      this.form.name = this.admin.name,
      this.form.lastname = this.admin.lastname
    },
    onSubmit(event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    }
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
  font-size: 0.80rem;
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
  border-radius: 4px;
  font-size: 0.75rem;
  font-weight: 400;
  color: #FFFFFF;
  text-decoration: none;
  background-color: #ad0202;
  padding: 5px;
  border: none;
  outline: none;
  cursor: pointer;
  margin-right: 6px;
}
.carta-footer__botones--cancelar:hover {
  background-color: #8f0303;
}
.carta-footer__botones--boton {
  font-family: 'Roboto', sans-serif;
  border-radius: 4px;
  font-size: 0.75rem;
  font-weight: 400;
  color: #FFFFFF;
  background-color: #485EB2;
  padding: 5px;
  border: none;
  outline: none;
  cursor: pointer;
}
.carta-footer__botones--boton:hover {
  background-color: #3f529c;
}
.titulo-modal{
  font-family: 'Roboto', sans-serif !important;
}
.boton-modal-a{
  background-color: #485EB2;
  border: none;
  margin-left: 12px;
  padding-top: 5px !important;
}
.boton-modal-b{
  background-color: #ad0202;
  border: none;
  padding-top: 5px !important;
}
</style>
