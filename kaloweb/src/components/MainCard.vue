<script>
import {ref, useTemplateRef} from 'vue';
    export default {
        name: "MainCard",
        props: {
            text: {
                type: String,
                default:"kaloweb"
            }
        },
        data() {
            return {
            }
        },
        computed: {},
        methods: {
            },
        watch: {},
        emits: {}}
</script>

<template>
    <div class="pieces">
        <div class="piece1" ref="piece1">
            <div v-for="(letter, index) in text" :key="index" :class="letter" class="letter">{{ letter }}</div>
        </div>
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
    grid-template-areas: "piece1 card .";
    grid-template-columns: 85px 55vw;
    gap: 75px;
    .card{
        grid-area: card;
        min-inline-size: 55vw;
        min-block-size: 75vh;
        max-inline-size: 75vw;
        padding-block-end: 1%;
        color: var(--txtColor);
        border: var(--general-border);
        background-color: var(--card-bg);
        box-shadow: 4px 4px 2px #000 inset;
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
    position: relative;
    z-index: 1;
    --informaticGreen: rgb(0, 210, 0);
    grid-area: piece1;
    border-radius: 50px;
    margin-inline-start: 10px;
    background-image: var(--display-bg);
    min-inline-size: 10px;
    min-block-size: 10px;
    color: var(--card-bg);
    .letter{
        font-size: 20px;
        position: relative;
        z-index: -2;
        translate: 40% -695%;
        /* animation: fallingLetters 2s linear forwards; */
    }
    .K{
        animation: fallingLetters 2s 6s linear forwards;
    }
    .a{
        animation: fallingLetters 2s 5s linear forwards;
    }
    .l{
        animation: fallingLetters 2s 4s linear forwards;
    }
    .o{
        animation: fallingLetters 2s 3s linear forwards;
    
    }
    .w{
        animation: fallingLetters 2s 2s linear forwards;
    }
    .e{
        animation: fallingLetters 2s 1s linear forwards;
    }
    .b{
        animation: fallingLetters 2s linear forwards;
    }
}
}

@keyframes fallingLetters {
  0%{
    color: var(--card-bg);
    transform: translateY(-695%);
  }
  66%{
    color: var(--card-bg);
  }
  100%{
    color: var(--informaticGreen);
    transform: translateY(1200%);
  }
}
</style>