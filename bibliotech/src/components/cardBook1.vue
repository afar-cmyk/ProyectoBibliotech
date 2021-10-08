<template>
  <div>
    <div class="option-book" v-b-modal.modal-book1>
      <!--Imagen de categoría-->
      <img class="img-option" src="../assets/images/manual.png" fluid-grow alt="Un libro"/>
        <figcaption class="data-book"> <!--Datos del libro-->
          <h4>Título: Los cuentos como son</h4> <!--Título-->
          <h5>Autor: Rudyard Kipling</h5> <!--Autor-->
        </figcaption>
    </div>
    <!--Modal con más información del libro y solicitud-->
    <b-modal id="modal-book1" size="sm" centered ok-only hide-footer no-stacking> 
      <p class="info-book"><!--Datos extra-->
        Formato: Ilustración <br />Viaje al centro de la tierra <br />Julio
        Verne <br />2004 <br />Panamericana Editorial <br />ISBN
        978-9-58300-688-3 <br /><b>Disponible</b>
      </p>
      <div class="btn-solitude">  
        <b-button v-b-modal.modal-solitude1>Solicitar</b-button><!--Botón solicitar-->
      </div>
    </b-modal>
    <!--Modal con confirmación, se puede reemplazar por el plugin de sweet alert-->
    <b-modal id="modal-solitude1" size="sm" centered ok-only hide-footer>
      <div class="confirmed-box">
        <div class="box-check">
          <p class="confirmed-text">¡Su préstamo ha sido exitoso!</p>
          <div class ="confirmed-icon">
            <b-icon icon="check-circle"></b-icon>
          </div>
        </div>
      </div>
    </b-modal>
  </div>
</template>
<style>
  .btn-secondary{
      background-color: #485eb2 !important;
      border: 1px solid #485eb2 !important;
  }
  /*Modal 1 solo cambia .modal-view*/
  .modal-view{
      display: flex;
      flex-wrap: wrap;
      flex-direction: row;
      justify-content: center;
  }
  .modal-header{
      background-color: #ff3000 !important;
      border-bottom: none !important;
  }
  .close{
      font-size: 2rem !important;
      color: #FFF !important;
      text-shadow: none !important;
      opacity: none !important;
      background-color: #ff6c38 !important;
  }
  .close:hover{
    color: #001154 !important;
  }
  .modal-backdrop{
    background-color: #FFF !important;
  }
  /*Organización de los libros*/
  .option-book{
    margin-top: 1rem;
  }
  .option-book:hover{
   background-color: #d6d6d669;
  }
  .img-option{
    width: 50%;
  }
</style>
