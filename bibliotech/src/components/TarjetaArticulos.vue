<template>
    <!-- Carta para listar elementos -->
                        <div class="carta">

                            <!-- Seccion superior de la carta -->
                            <div class="carta-header">
                                <div class="carta-header__texto">
                                    <p class="carta-header__texto carta-header__texto--titulo">Nombre del Articulo</p>
                                    <p class="carta-header__texto carta-header__texto--subtitulo">Nombre del Autor</p>
                                </div>
                            </div>

                            <!-- Seccion central de la carta -->
                            <div class="carta-body">
                                <div class="carta-body__imagen">
                                    <img src="assets/images/illustrated/book-one.png" alt="">
                                </div>
                            </div>

                            <!-- Seccion inferior de la carta -->
                            <div class="carta-footer">
                                <div class="carta-footer__botones">
                                    <a class="carta-footer__botones carta-footer__botones--cancelar"
                                        href="item.html">BORRAR</a>
                                    <input class="carta-footer__botones carta-footer__botones--boton" type="submit"
                                        value="EDITAR" onclick="javascript:enlaceEditarArticulo()">
                                </div>
                            </div>


                        </div>
                        <!-- FIN Carta para listar elementos -->
</template>
<style scoped>
.carta {
    /* background-color: #FF3000;  wireframe*/

    background-color: #ffffff;
    display: flex;
    flex-direction: column;


    width: 316px;
    height: 280px;
    border-radius: 7px;

    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);

    box-sizing: border-box;

    margin-top: 2px;
}
.carta-header {
    /* background-color: chartreuse; */
    height: 68px;
    width: 100%;
    display: flex;
    align-items: center;
}
.carta-header__texto {
    /* background-color: #FF3000; WIREFRAME*/

    height: 42px;
    width: 100%;

    display: flex;
    flex-direction: column;
    justify-content: center;

    padding-left: 1rem;

    box-sizing: border-box;

}
.carta-header__texto--titulo {
    /* background-color: #757575; WIREFRAME*/

    font-family: "Roboto";
    font-size: 1rem;
    font-weight: 500;
    padding: 0%;
    margin: 0%;
}
.carta-header__texto--subtitulo {
    /* background-color: #AAAAAA; WIREFRAME*/

    font-family: "Roboto";
    font-size: 0.75rem;
    font-weight: 300;
    padding: 0%;
    margin: 0%;
}
.carta-body {
    background-color: #E6E6E6;

    height: 178px;
    display: flex;
    justify-content: center;
}
.carta-body__imagen {
    display: flex;
    flex-direction: column;
    justify-content: center;
    overflow: hidden;
    max-height: 174px;
    box-sizing: border-box;
}
.carta-body img {
    /* background-color: #03DAC5; WIREFRAME*/
    max-width: 100%;
    height: auto;
}
.carta-footer {
    /* background-color: cyan; WIREFRAME*/

    height: 40px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
}
.carta-footer__botones {
    /* background-color: #FFAA00; WIREFRAME*/
    display: flex;
    flex-direction: row;
    align-items: center;


}
.carta-footer__botones--cancelar {
    color: #FF6C38;
    font-size: 0.75rem;
    text-decoration: none;
}
.carta-footer__botones--cancelar:hover {
    color: #da5e31;
}
.carta-footer__botones--boton {

    border-radius: 4px;
    font-size: 0.625rem;
    font-weight: 400;
    color: #FFFFFF;
    background-color: #485EB2;

    margin-left: 7px;
    padding: 6px;
    border: none;
    outline: none;
    cursor: pointer;
}
.carta-footer__botones--boton:hover {
    background-color: #3f529c;
}
</style>