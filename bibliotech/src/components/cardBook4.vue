<template>
  <div>
    <div class="option-book" v-b-modal.modal-book4>
      <!--Imagen de categoría-->
      <img class="img-option" src="../assets/images/academic.png" fluid alt="Un libro"/>
      <figcaption class="data-book"> <!--Datos del libro-->
        <h4>Título: Los cuentos como son</h4> <!--Título-->
        <h5>Autor: Rudyard Kipling</h5> <!--Autor-->
      </figcaption>
    </div>
    <!--Modal con más información del libro y solicitud-->
    <b-modal id="modal-book4" size="sm" centered ok-only hide-footer no-stacking> 
      <p class="info-book"><!--Datos extra-->
        Formato: Ilustración <br />Viaje al centro de la tierra <br />Julio
        Verne <br />2004 <br />Panamericana Editorial <br />ISBN
        978-9-58300-688-3 <br /><b>Disponible</b>
      </p>
      <div class="btn-solitude">
        <b-button v-b-modal.modal-solitude4>Solicitar</b-button><!--Botón solicitar-->
      </div>
    </b-modal>
    <!--Modal con confirmación, se puede reemplazar por el plugin de sweet alert-->
    <b-modal id="modal-solitude4" size="sm" centered ok-only hide-footer>
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
