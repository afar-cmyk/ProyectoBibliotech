<template>
    <router-link class="contenedor-barra" tag="div" :class="[ status ? 'contenedor-barra--actual' : '' ]" :to=view>
        <div class="sideBar_elemento">
            <div class="sideBar_elemento__icono" >
                <span class="material-icons material-icons--settings" :class="[ status ? 'material-icons--settings-actual' : '' ]">{{ icon }}</span>
            </div>
            <p class="sideBar_elemento__titulo mb-0" :class="[ status ? 'sideBar_elemento__titulo--actual' : '' ]">{{ title }}</p>
        </div>
    </router-link>
</template>
<script>
export default {
    props: {
        title: {
            type: String,
            default: () => ''
        },
        icon: {
            type: String,
            default: () => ''
        },
        status: {
            type: Boolean,
            default: () => false
        },
        view: {
            type: String,
            default: () => ''
        }
    }
}
</script>
<style>
@media (min-width: 1234px) { 
  .usuario_titulo {
    font-size: 80%;
  }
  .sideBar_elemento__titulo{
        font-size: 93%;
  }
  
}
@media (min-width: 1367px) { 
  .sideBar_elemento__titulo{
        font-size: 100%;
  }
}
@media (max-width: 1233px) { 
  .sideBar_elemento__titulo {
    display: none !important;
  }
.sideBar_elemento{
    justify-content: space-around;
}
.sideBar_elemento__icono{
    margin-right: 0;
}
}
</style>