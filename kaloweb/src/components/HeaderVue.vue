<script>
  export default {
    name: "HeaderVue"
  }
</script>

<template>
    <header>        
            <div class="title-container">
                <h1 class="head">Kaloweb</h1>
        </div>
        <nav>
           <ul>
            <div class="element-container">
              <li><a href="#">Inicio</a></li>
            </div>
            <div class="element-container">
              <li><a href="../../proyectos/index.html">Proyectos</a></li>
            </div>
            <div class="element-container">
              <li><a href="trabajos.html">Trabajos</a></li>
            </div>
            <div class="element-container">
              <li><a href="estudios.html">Estudios</a></li>
            </div>
            <div class="element-container">
              <li><a href="aficiones.html">Aficiones</a></li>
            </div>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
header{
  --general-border: 5px solid var(--txtColor);
  --border-hover: 5px solid rgb(0, 210, 0);
  --informaticGreen: rgb(0, 210, 0);
  --card-bg: rgb(207, 207, 207);
  --txtColor: #292929;
  --hoverLinkColor: #6f6f6f;
  --buttonBgColor: #6a6a6a;
  --shadowColor: rgb(179, 179, 179);
  --lightShadowColor: rgb(255, 249, 249);
  position: relative;
  z-index: 3;
  inline-size: 100%;
  margin-block: 0;
    .title-container{
      inline-size: 45%;
      background-color: var(--card-bg);
      border: var(--general-border);
      .head{
        font-size: 3.2em;
        line-height: 1.1;
        padding-block: 2% 5%;
        margin-block: 5% 0%;
        margin-inline-start: 5%;
        color: var(--txtColor);
      }
    }
    nav{
  inline-size: 100%;
  margin-block: 7%;
  margin-inline-start: 0;
  ul{
    display: flex;
    justify-content: space-evenly;
    inline-size: 100%;
    padding-inline-start: 0;
    .element-container{
      padding: 2px;
      background-color: var(--buttonBgColor);
      border-radius: 5px;
      box-shadow: 2px 2px 2px #000 inset;
      &:hover{
        --buttonsShadowContorn: 2px 2px 1px var(--informaticGreen);
        background-color: var(--informaticGreen); 
      }
      li{
        list-style-type: none;
        background-color: var(--card-bg);
        transition: all 0.5s linear;
        border-radius: 5px;
        box-shadow: -4px -4px 3px var(--shadowColor) inset,
        2px 2px 3px var(--lightShadowColor) inset;
        &:hover{
          filter: drop-shadow(2px 2px 0 var(--informaticGreen));
          cursor: pointer;
        }
        a{
          line-height: 40px;
          padding-inline: 5px;
          color: var(--txtColor);
          transition: all 0.5s linear;
          &:hover{
            color: var(--informaticGreen);
            text-shadow: 0 0 1px var(--informaticGreen);
          }
        }
      }
    }
    } 
}
  }
</style>