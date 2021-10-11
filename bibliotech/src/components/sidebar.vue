<template>
  <div>
    <!-- Grupo de elementos #1 -->
    <div class="d-flex flex-column justify-content-around contenedor-header">
      <!-- Contenedor logo -->
      <div class="contenedor-header__logo">
        <img src="../assets/images/logo-minimal.png" alt="Logo Bibliotech" />
      </div>

      <!-- Contenedor de usuario actual -->
      <div
        class="d-flex flex-column justify-content-around contenedor-header__usuario"
      >
        <div
          class="d-flex justify-content-between align-items-center header__usuario"
        >
          <!-- Nombre de usuario actual -->
          <p class="d-flex usuario_titulo mb-0">
            Nombre de usuario
          </p>

          <!-- Tipo de usuario actual -->
          <labelRoot />
          <!-- FIN Tipo de usuario actual -->
        </div>
      </div>
    </div>
    <!-- FIN Grupo de elementos #1 -->

    <!-- Grupo de elementos #2 -->
    <div class=" contenedor-body-1">
      <navItem :status="option == 1 ? true : false" title="Recientes" icon="restore" view="Newer"/>
      <navItem :status="option == 2 ? true : false" title="Artículos" icon="import_contacts" view="Item"/>
      <navItem :status="option == 3 ? true : false" title="Administradores" icon="group" view="Admin"/>          
    </div>
    <!-- FIN Grupo de elementos #2 -->

    <!-- Grupo de elementos #3 -->
    <div class="contenedor-body-2">
        <navItem title="Salir" icon="logout" view="Login"/>
    </div>
    <!-- FIN Grupo de elementos #3 -->
  </div>
</template>

<script>
// Labels //
import labelRoot from "./labelRoot.vue"
import labelAdmin from "./labelAdmin.vue"
import navItem from "./sideBar/navItem.vue"

export default {
  components: {
    labelRoot,
    labelAdmin,
    navItem,
  },
  props: {
    option: {
      type: Number,
      default: () => 1
    }
  }, 
  methods: {
    changeStatus(i) {
      this.status = i
      console.log(i)
    }
  }
};
</script>

<style scoped>
.contenedor-header {
  width: 100%;
  height: 9vw;
  border-bottom: 1px solid #0000001f;
}
.contenedor-header__logo {
  width: 100%;
  height: 100%;
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  padding-top: 1.25rem;
  box-sizing: border-box;
}
.contenedor-header__logo img {
  width: 100%;
}
.contenedor-header__usuario {
  width: 100%;
  height: 2.5rem;
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  box-sizing: border-box;
}
.header__usuario {
  padding: 0;
  width: 100%;
  height: 1.25rem;
}
.usuario_titulo {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  margin-bottom: 0;
}
.contenedor-body-1 {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  width: 100%;
  height: 10rem;
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  border-bottom: 1px solid #0000001f;
  box-sizing: border-box;
}
.contenedor-body-2 {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 3.75rem;
  padding-top: 0.625rem;
  padding-left: 0.625rem;
  padding-right: 0.625rem;
  box-sizing: border-box;
}
</style>
