<template>
    <div class="container-migas d-flex flex-row align-items-center">
        <p class="mb-0 texto-migas"><a class="ancla" href="">Artículos</a></p>
        <p class="separador mb-0 texto-migas">/</p>
        <p class="actual mb-0 texto-migas ">Nuevo Artículo</p>
    </div>
</template>
<script>
export default {
    setup() {
        
    },
}
</script>
<style scoped>
.container-migas {
    height: 100%;
}
.texto-migas {
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
    font-size: 2.125rem;
    letter-spacing: 0.016rem;
}
.texto-migas a {
    text-decoration: none;
    color: #AAAAAA
}
.texto-migas a:hover {
    text-decoration: none;
    color: #485EB2
}
.separador {
    color: #AAAAAA;
    padding-left: 2rem;
    padding-right: 2rem;
}
</style>