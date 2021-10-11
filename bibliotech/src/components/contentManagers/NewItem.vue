<template>
    <!-- Recuadro que contiene a todos los elementos del formulario -->
            <div class="formulario-base">

                <!-- Segmento izquiero del contenedor -->
                <div class="formulario-base-lado1">
                    <label for="isbn">ISBN:</label>
                    <input type="text" id="isbn" name="isbn">

                    <label for="nombre-articulo">Nombre del artículo:</label>
                    <input type="text" id="nombre-articulo" name="nombre-articulo">

                    <label for="nombre-autor">Nombre del autor:</label>
                    <input type="text" id="nombre-autor" name="nombre-autor">
                </div>
                <!-- FIN Segmento izquero del contenedor -->


                <!-- Segmento derecho del contenedor -->
                <div class="formulario-base-lado2">
                    <label for="nombre-editorial">Nombre de la editorial:</label>
                    <input type="text" id="nombre-editorial" name="nombre-editorial">

                    <label for="nombre-editorial">Seleccione una categoria:</label>
                    <select name="categoria" id="categoria">
                        <option value=""></option>
                        <option value="Académico">Académico</option>
                        <option value="Digital">Digital</option>
                        <option value="Ilustración">Ilustración</option>
                        <option value="Manual">Manual</option>
                        <option value="Revista">Revista</option>
                    </select>
                </div>
                <!-- FIN Segmento derecho del contenedor -->

                <!-- Sección inferior del contenedor -->
                <div class="contenedor-formulario-footer">

                    <div class="contenedor-botones">
                        <a class="enlace-cancelar" href="item.html">CANCELAR</a>
                        <input class="formulario__boton-crear" type="submit" value="CREAR">
                    </div>

                </div>
                <!-- FIN Sección inferior del contenedor -->

            </div>
            <!-- FIN Recuadro que contiene a todos los elementos del formulario -->
</template>

<style scoped>
.formulario-base {
    background-color: rgb(255, 255, 255);
    display: flex;
    flex-flow: wrap;
    width: 53rem;
    height: 25rem;
    border-radius: 4px;
    border: 1px solid #0000001F;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    font-weight: 300;
    font-family: 'Roboto', sans-serif;
}
.formulario-base-lado1 {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    width: 26.5rem;
    height: 21.438rem;
    padding-top: 2.5rem;
    padding-left: 2.5rem;
    padding-right: 2.5rem;
    box-sizing: border-box;
}
.formulario-base-lado2 {
    display: flex;
    flex-direction: column;
    justify-content: normal;
    width: 26.5rem;
    height: 21.438rem;
    padding-top: 2.5rem;
    padding-left: 2.5rem;
    padding-right: 2.5rem;
    box-sizing: border-box;
}
.formulario-base-lado1 input {
    width: 21.313rem;
    height: 2.5rem;
    margin-bottom: 60px;
    border-radius: 4px;
    box-sizing: border-box;
}
.formulario-base-lado2 input {
    width: 21.313rem;
    margin-bottom: 60px;
    border-radius: 4px;
    box-sizing: border-box;
}
.formulario-base-lado2 select {
    width: 21.313rem;
    margin-bottom: 60px;
    box-sizing: border-box;
}
.contenedor-formulario-footer {
    display: flex;
    justify-content: end;
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
