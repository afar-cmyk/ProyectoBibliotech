<template>
    <div class="contenedor-botonessuperiores">

              <!-- Boton para crear elementos -->
              <div v-b-modal.modal-creation  class="boton__crear">
                <!-- <div v-b-modal="`modal-${index}` " @click="editItem()" class="boton__crear"> -->
                <div class="icono-superior">
                    <span class="mb-0 material-icons material-icons--boton-sup">add</span>
                </div>
              </div> <!-- FIN Boton para crear elementos -->

    <b-modal id="modal-creation" title="Nuevo Artículo" hide-footer centered>
      <!-- <b-modal class="titulo-modal" :id="`modal-${index}`" title="Nuevo Artículo" hide-footer> -->

        <b-form @submit="onSubmit">   
        <b-container>  
            <b-row>
            <b-col>
                <div class="form-floating mt-4 mb-4">
                    <input v-model="form.book_isbn" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                    <label label for="mb-0 floatingInput" class="text-secondary">ISBN</label>
                </div>
            </b-col>
            </b-row>

            <b-row>
            <b-col>
                <div class="form-floating mb-4">
                    <input v-model="form.book_title" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                    <label label for="mb-0 floatingInput" class="text-secondary">Nombre del artículo</label>
                </div>
            </b-col>
            </b-row>

            <b-row>
            <b-col>
                <div class="form-floating mb-4">
                    <input v-model="form.book_author" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                    <label label for="mb-0 floatingInput" class="text-secondary">Nombre del autor</label>
                </div>
            </b-col>
            </b-row>

            <b-row>
            <b-col>
                <div class="form-floating mb-4">
                    <input v-model="form.book_publisher" type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                    <label label for="mb-0 floatingInput" class="mb-0 text-secondary">Nombre de la editorial</label>
                </div>
            </b-col>
            </b-row>

            <b-row>
            <b-col>
                <div class="form-floating">
                    <select class="mb-0 selector form-select" id="floatingSelectGrid" aria-label="Floating label select example">
                        <option selected>Seleccione una categoria</option>
                        <option value="1">Académico</option>
                        <option value="2">Digital</option>
                        <option value="3">Ilustración</option>
                        <option value="4">Manual</option>
                        <option value="5">Revista</option>
                    </select>
                    <label for="floatingSelectGrid">Categoria</label>
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
</template>
<script>
export default {
  props: {
    item: {
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
        book_isbn: '',
        book_title: '',
        book_author: '',
        book_publisher: '',
        book_genre: ''
      }
    }
  },
  methods: {
    editItem() {
      console.log(this.item)
      this.form.book_isbn = this.item.book_isbn,
      this.form.book_title = this.item.book_title,
      this.form.book_author = this.item.book_author,
      this.form.book_publisher = this.item.book_publisher,
      this.form.book_genre = this.item.book_genre
    },
    onSubmit(event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    },
  },
}
</script>
<style scoped>
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
.titulo-modal{
  font-family: 'Roboto', sans-serif !important;
}
.boton-modal-a{
  background-color: #485EB2;
  border: none;
  margin-left: 12px;
}
.boton-modal-b{
  background-color: #ad0202;
  border: none;
}
</style>
