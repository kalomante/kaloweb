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
               <li><a href="#">Inicio</a></li>
               <li><a href="../../proyectos/index.html">Proyectos</a></li>
               <li><a href="trabajos.html">Trabajos</a></li>
               <li><a href="estudios.html">Estudios</a></li>
               <li><a href="aficiones.html">Aficiones</a></li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
header{
  --general-border: 5px solid var(--txtColor);
  --border-hover: 5px solid rgb(0, 210, 0);
  --card-bg: rgb(229, 229, 229);
  --txtColor: #292929;
  --hoverLinkColor: #6f6f6f;
  /* position: absolute; */
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
    li{
      list-style-type: none;
      background-color: var(--card-bg);
      transition: all 0.5s linear;
      box-shadow: 2px 2px 1px #595959, 3px 3px 1px rgb(241, 241, 241) inset;
      a{
        line-height: 40px;
        padding-inline: 5px;
        color: var(--txtColor);
        transition: all 0.5s linear;
        &:hover{
          color: var(--hoverLinkColor);
        }
      }
    }
  } 
}
  }
</style>