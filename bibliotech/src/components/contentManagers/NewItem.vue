<template>
    <!-- Recuadro que contiene a todos los elementos del formulario -->
            <b-container class="formulario-base d-flex flex-wrap">
                <b-row>
                    <b-col class="formulario-base-lado">
                        <div class="form-floating mt-0 mb-5">
                            <input type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                            <label label for="mb-0 floatingInput" class="text-secondary">ISBN</label>
                        </div>

                        <div class="form-floating mb-5">
                            <input type="email" class="mb-0 form-control" id="floatingInput" placeholder="">
                            <label label for="mb-0 floatingInput" class="text-secondary">Nombre del artículo</label>
                        </div>

                        <div class="form-floating">
                            <input type="email" class="mb-0 form-control" id="floatingInput" placeholder="">
                            <label label for="mb-0 floatingInput" class="text-secondary">Nombre del autor</label>
                        </div>
                    </b-col>

                    <b-col class="formulario-base-lado">
                        <div class="form-floating mt-0 mb-5">
                            <input type="text" class="mb-0 form-control" id="floatingInput" placeholder="">
                            <label label for="mb-0 floatingInput" class="mb-0 text-secondary">Nombre de la editorial</label>
                        </div>

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

                <b-row class="contenedor-formulario-footer">

                </b-row>
            </b-container >
            <!-- FIN Recuadro que contiene a todos los elementos del formulario -->
</template>

<style scoped>
.formulario-base {
    display: flex !important;
    background-color: rgb(255, 255, 255);
    width: 53rem;
    height: 25rem;
    border-radius: 4px;
    border: 1px solid #0000001F;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    font-weight: 300;
    font-family: 'Roboto', sans-serif;
}
.formulario-base-lado{
    width: 26.5rem;
    height: 21.438rem;
    padding-top: 2.5rem;
    padding-left: 2.5rem;
    padding-right: 2.5rem;
    box-sizing: border-box;
}
.contenedor-formulario-footer {
    width: 100%;
    padding-top: 0.625rem;
    padding-bottom: 0.625rem;
    border-top: 1px solid #0000001F;
    box-sizing: border-box;
}
.contenedor-botones {
    display: flex;
    align-items: center;
    padding-right: 2.5rem;
}
.contenedor-botones input {
    margin-left: 0.625rem;
}
.enlace-cancelar {
    color: #FF6C38;
    font-size: 0.875rem;
    text-decoration: none;
    margin-bottom: 3px;
}
.enlace-cancelar:hover {
    color: #da5e31;
}
.formulario__boton-crear {
    width: 5rem;
    height: 2.5rem;
    border-radius: 4px;
    font-size: 0.875rem;
    color: #FFFFFF;
    background-color: #485EB2;
    border: none;
    outline: none;
    margin-bottom: 3px;
    cursor: pointer;
}
.formulario__boton-crear:hover {
    background-color: #3f529c;
}
</style>
