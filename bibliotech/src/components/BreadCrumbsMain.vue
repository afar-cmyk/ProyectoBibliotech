<template>
    <div class="container-migas d-flex flex-row align-items-center">
        <p class="actual mb-0 texto-migas ">{{ title }}</p>
        <p class="separador mb-0 texto-migas">|</p>
    </div>
</template>
<script>
export default {
    props: {
        title: {
            type: String,
            default: () => ''
        }
    }
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
.separador {
    color: #AAAAAA;
    padding-left: 2rem;
    padding-right: 2rem;
}
</style>
