<template>
  <div class="header__usuario-label">
    <b-badge class="usuario-label-texto">Admin</b-badge>
  </div>
</template>
<style scoped>
.header__usuario-label {
  background-color: #7575753b !important;
  display: inline-flex;
  border-radius: 4px;
}
.usuario-label-texto {
  font-family: "Roboto", sans-serif;
  font-weight: 300;
  color: #7e7e7e;
}
@media (min-width: 1234px) { 
  .usuario-label-texto {
    font-size: 70%;
  }
}
@media (min-width: 1367px) { 
  .usuario-label-texto {
    font-size: 100%;
  }
}
</style>
