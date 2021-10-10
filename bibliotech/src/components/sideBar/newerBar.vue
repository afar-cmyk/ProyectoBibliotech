<template>
  <!-- Primer elemento de la barra lateral -->
  <div class="contenedor-barra" :class="[ status ? 'contenedor-barra--actual' : '' ]">
    <div class="sideBar_elemento">
      <div class="sideBar_elemento__icono">
        <span class="material-icons material-icons--settings" :class="[ status ? 'material-icons--settings-actual' : '' ]">restore</span>
      </div>
      <p class="sideBar_elemento__titulo mb-0" :class="[ status ? 'sideBar_elemento__titulo--actual' : '' ]">Recientes</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    status: {
      type: Boolean,
      default: () => false
    }
  }
}
</script>
<style scoped></style>
