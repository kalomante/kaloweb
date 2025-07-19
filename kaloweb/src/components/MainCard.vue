<script>
    export default {
        name: "MainCard"
    }
</script>

<template>
    <div class="pieces">
        <div class="piece1"></div>
        <section class="card">
            <article class="life">
                <h2 class="section-title">Vida</h2>
                <p>Nací en un pequeño pueblo costero de Galicia. Mi padre fue marinero y mi madre trabajó como cuidadora. Desde que era pequeño, siempre tuve una afición por los videojuegos y las series de animación. Al salir del instituto entré en la Universidad de Santiago de Compostela, donde me gradué en Filología Inglesa. Sin embargo, no seguí con el máster, y tras pasar dos años estudiando para opositar como bibliotecario, me puse a trabajar como camarero para poder cotizar y ganarme un salario. Fue durante el tiempo que me pasé estudiando para bibliotecario que descubrí el interesante mundo del desarrollo y la programación. En un curso organizado por el Servicio de Empleo Público del Estado, aprendí conceptos básicos de programación, publicación y desarrollo de páginas web. Durante las 480 horas que duró el curso, entré en contacto con tecnologías como HTML5, CSS3 y JS, lo que me animó finalmente a cursar un Ciclo Superior de Desarrollo de Páginas Web.</p>
            </article>
        </section>
    </div>
    </template>

<style>
:root{
    --txtColor: #292929;
    --card-bg: rgb(229, 229, 229);
    --general-border: 5px solid var(--txtColor);
    --display-bg: radial-gradient(ellipse, #000, #1c0a51);
}
.pieces{
    display: grid;
    grid-template-areas: "piece1 card";
    grid-template-columns: 12vw 55vw;
    gap: 20px;
    .card{
        grid-area: card;
        margin: 0 auto;
        min-inline-size: 55vw;
        min-block-size: 75vh;
        max-inline-size: 75vw;
        padding-block-end: 1%;
        color: var(--txtColor);
        border: var(--general-border);
        background-color: var(--card-bg);
        .life{
            padding-inline: 15px;
            
            .section-title{
                font-size: 40px;
                text-align: center;
                border-bottom: thin solid #292929;
                
            }
            p{
                text-align: justify;
                text-indent: 30px;
            }
        }
}

.piece1{
    grid-area: piece1;
    border-radius: 50px;
    margin-inline-start: 10px;
    background-image: var(--display-bg);
    min-inline-size: 10px;
    min-block-size: 10px;
}
}
</style>