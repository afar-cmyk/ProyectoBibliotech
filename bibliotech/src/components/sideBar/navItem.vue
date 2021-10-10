<template>
    <div class="contenedor-barra" :class="[ status ? 'contenedor-barra--actual' : '' ]" to="Newer">
        <div class="sideBar_elemento">
            <div class="sideBar_elemento__icono" >
                <span class="material-icons material-icons--settings" :class="[ status ? 'material-icons--settings-actual' : '' ]">{{ icon }}</span>
            </div>
            <p class="sideBar_elemento__titulo mb-0" :class="[ status ? 'sideBar_elemento__titulo--actual' : '' ]">{{ title }}</p>
        </div>
    </div>
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
        }
    }
}
</script>