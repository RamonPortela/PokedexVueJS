<template>
  <div id="app">
      <div class="container">
          <router-view></router-view>
      </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      pokemonSelecionado: null,
      pronto: false,
    }
  },
  methods:{
      selecionarPokemon(pokemon){
        this.pokemonSelecionado = pokemon;
      },
      voltar(){
          this.pokemonSelecionado = null;
      }
  },
  computed:{
      exibirDetalhes(){
          if(this.pokemonSelecionado == null)
              return false;
          else
              return true;
      }
  }
}
</script>

<style>
    .holder{
        background: white;
        padding: 15px;
        border-radius: 15px;
        margin: auto;
        border: 1px solid black;
        box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    }

    @keyframes slide-in{
        0%{
        }
        100%{
            top:-100%;
        }
    }

    @keyframes slide-out{
        0%{
            top:500%
        }
        100%{

        }
    }


#app {

  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: auto;
  margin-right: auto;
  width: 85%;
  background-color: transparent;
  padding: 10px 0 10px 0;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

body{
  background: #f1f1f1;
}

    @keyframes rotateBall {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
    }
    @-webkit-keyframes rotateBall {
        0% {
            transform: rotate(0deg);
        }
        50% {
            transform: rotate(50deg);
        }
        0% {
            transform: rotate(360deg);
        }
    }

    .div-tipo{
        border-radius: 30px;
        width: 75px;
        padding: 2px;
        color: white;
        font-weight: 600;
        background-clip: border-box;
        box-shadow: 1px 1px 1px black;
        display: inline-block;
        margin-left: 5px;
        cursor: pointer;
        margin-top: 10px;
    }

    tr{
        border-bottom: 1px solid #adc2bf;
        border-top: 1px solid #adc2bf;

    }

    th{
        width: 100%
    }

    table {
        border-collapse: collapse;
        margin:auto;
        width: 100%;
    }

    .td-nome{
        width: 65%;
        text-align: left;
    }

    .td-valor{
        text-align: center;
    }


    .seletor-pokemon{
        cursor: pointer;
    }

    .seletor-pokemon:hover{
        background-color: azure;
    }

    .active{
        background-color: beige;
    }

    .fire{
        background-color: #f95343;
    }
    .normal{
        background-color: #BCBCAF;
    }
    .poison{
        background-color: #AB5EA2;
    }
    .psychic{
        background-color: #fa5489;
    }
    .grass{
        background-color: #8CD751;
    }
    .ground{
        background-color: #EDCB56;
    }
    .ice{
        background-color: #96F1FF;
    }
    .rock{
        background-color: #CDBD72;
    }
    .dragon{
        background-color: #993aff;
    }
    .water{
        background-color: #56AEFF;
    }
    .bug{
        background-color: #C3D21F;
    }
    .dark{
        background-color: #8F6956;
    }
    .fighting{
        background-color: #A85645;
    }
    .ghost{
        background-color: #7874D6;
    }
    .steel{
        background-color: #C3C2D8;
    }
    .flying{
        background-color: #79A4FF;
    }
    .electric{
        background-color: #FDE53C;
    }
    .fairy{
        background-color: #ffb0c5;
    }

    .div-carregando{
        top: 50px;
        text-align: center;
        position: absolute;
        left: 35%;
    }

    #loading {
        height: 48px;
        width: 264px;
        position: absolute;
        left: 50%;
        transform: translateX(-50%) translateY(-50%);
    }

    .pokeball {
        width: 4px;
        height: 4px;
        transform-origin: 24px 24px;
        animation: rotateBall 1.5s infinite forwards;
    }
    .pokeball#normal {
        box-shadow: 16px 0 0 #000, 20px 0 0 #000, 24px 0 0 #000, 28px 0 0 #000, 8px 4px 0 #000, 12px 4px 0 #000, 16px 4px 0 #e20f07, 20px 4px 0 #e20f07, 24px 4px 0 #e20f07, 28px 4px 0 #e20f07, 32px 4px 0 #000, 36px 4px 0 #000, 4px 8px 0 #000, 8px 8px 0 #e20f07, 12px 8px 0 #e20f07, 16px 8px 0 #FFF, 20px 8px 0 #e20f07, 24px 8px 0 #e20f07, 28px 8px 0 #e20f07, 32px 8px 0 #e20f07, 36px 8px 0 #e20f07, 40px 8px 0 #000, 4px 12px 0 #000, 8px 12px 0 #e20f07, 12px 12px 0 #FFF, 16px 12px 0 #FFF, 20px 12px 0 #FFF, 24px 12px 0 #e20f07, 28px 12px 0 #e20f07, 32px 12px 0 #e20f07, 36px 12px 0 #e20f07, 40px 12px 0 #000, 0px 16px 0 #000, 4px 16px 0 #e20f07, 8px 16px 0 #e20f07, 12px 16px 0 #e20f07, 16px 16px 0 #FFF, 20px 16px 0 #e20f07, 24px 16px 0 #e20f07, 28px 16px 0 #e20f07, 32px 16px 0 #e20f07, 36px 16px 0 #e20f07, 40px 16px 0 #e20f07, 44px 16px 0 #000, 0px 20px 0 #000, 4px 20px 0 #e20f07, 8px 20px 0 #e20f07, 12px 20px 0 #e20f07, 16px 20px 0 #e20f07, 20px 20px 0 #000, 24px 20px 0 #000, 28px 20px 0 #e20f07, 32px 20px 0 #e20f07, 36px 20px 0 #e20f07, 40px 20px 0 #e20f07, 44px 20px 0 #000, 0px 24px 0 #000, 4px 24px 0 #000, 8px 24px 0 #e20f07, 12px 24px 0 #e20f07, 16px 24px 0 #000, 20px 24px 0 #FFF, 24px 24px 0 #a5a5a5, 28px 24px 0 #000, 32px 24px 0 #e20f07, 36px 24px 0 #e20f07, 40px 24px 0 #000, 44px 24px 0 #000, 0px 28px 0 #000, 4px 28px 0 #FFF, 8px 28px 0 #000, 12px 28px 0 #000, 16px 28px 0 #000, 20px 28px 0 #a5a5a5, 24px 28px 0 #a5a5a5, 28px 28px 0 #000, 32px 28px 0 #000, 36px 28px 0 #000, 40px 28px 0 #a5a5a5, 44px 28px 0 #000, 4px 32px 0 #000, 8px 32px 0 #FFF, 12px 32px 0 #FFF, 16px 32px 0 #FFF, 20px 32px 0 #000, 24px 32px 0 #000, 28px 32px 0 #a5a5a5, 32px 32px 0 #a5a5a5, 36px 32px 0 #a5a5a5, 40px 32px 0 #000, 4px 36px 0 #000, 8px 36px 0 #a5a5a5, 12px 36px 0 #FFF, 16px 36px 0 #FFF, 20px 36px 0 #FFF, 24px 36px 0 #a5a5a5, 28px 36px 0 #a5a5a5, 32px 36px 0 #a5a5a5, 36px 36px 0 #a5a5a5, 40px 36px 0 #000, 8px 40px 0 #000, 12px 40px 0 #000, 16px 40px 0 #a5a5a5, 20px 40px 0 #a5a5a5, 24px 40px 0 #a5a5a5, 28px 40px 0 #a5a5a5, 32px 40px 0 #000, 36px 40px 0 #000, 16px 44px 0 #000, 20px 44px 0 #000, 24px 44px 0 #000, 28px 44px 0 #000;
    }
    .pokeball#great {
        animation-delay: 0.25s;
        margin: -4px 0 0 54px;
        box-shadow: 16px 0 0 #000, 20px 0 0 #000, 24px 0 0 #000, 28px 0 0 #000, 8px 4px 0 #000, 12px 4px 0 #000, 16px 4px 0 #278de1, 20px 4px 0 #278de1, 24px 4px 0 #278de1, 28px 4px 0 #278de1, 32px 4px 0 #000, 36px 4px 0 #000, 4px 8px 0 #000, 8px 8px 0 #e20f07, 12px 8px 0 #e20f07, 16px 8px 0 #278de1, 20px 8px 0 #278de1, 24px 8px 0 #278de1, 28px 8px 0 #278de1, 32px 8px 0 #e20f07, 36px 8px 0 #e20f07, 40px 8px 0 #000, 4px 12px 0 #000, 8px 12px 0 #e20f07, 12px 12px 0 #e20f07, 16px 12px 0 #e20f07, 20px 12px 0 #278de1, 24px 12px 0 #278de1, 28px 12px 0 #e20f07, 32px 12px 0 #e20f07, 36px 12px 0 #e20f07, 40px 12px 0 #000, 0px 16px 0 #000, 4px 16px 0 #278de1, 8px 16px 0 #278de1, 12px 16px 0 #e20f07, 16px 16px 0 #e20f07, 20px 16px 0 #278de1, 24px 16px 0 #278de1, 28px 16px 0 #e20f07, 32px 16px 0 #e20f07, 36px 16px 0 #278de1, 40px 16px 0 #278de1, 44px 16px 0 #000, 0px 20px 0 #000, 4px 20px 0 #278de1, 8px 20px 0 #278de1, 12px 20px 0 #278de1, 16px 20px 0 #278de1, 20px 20px 0 #000, 24px 20px 0 #000, 28px 20px 0 #278de1, 32px 20px 0 #278de1, 36px 20px 0 #278de1, 40px 20px 0 #278de1, 44px 20px 0 #000, 0px 24px 0 #000, 4px 24px 0 #000, 8px 24px 0 #278de1, 12px 24px 0 #278de1, 16px 24px 0 #000, 20px 24px 0 #FFF, 24px 24px 0 #a5a5a5, 28px 24px 0 #000, 32px 24px 0 #278de1, 36px 24px 0 #278de1, 40px 24px 0 #000, 44px 24px 0 #000, 0px 28px 0 #000, 4px 28px 0 #FFF, 8px 28px 0 #000, 12px 28px 0 #000, 16px 28px 0 #000, 20px 28px 0 #a5a5a5, 24px 28px 0 #a5a5a5, 28px 28px 0 #000, 32px 28px 0 #000, 36px 28px 0 #000, 40px 28px 0 #a5a5a5, 44px 28px 0 #000, 4px 32px 0 #000, 8px 32px 0 #FFF, 12px 32px 0 #FFF, 16px 32px 0 #FFF, 20px 32px 0 #000, 24px 32px 0 #000, 28px 32px 0 #a5a5a5, 32px 32px 0 #a5a5a5, 36px 32px 0 #a5a5a5, 40px 32px 0 #000, 4px 36px 0 #000, 8px 36px 0 #a5a5a5, 12px 36px 0 #FFF, 16px 36px 0 #FFF, 20px 36px 0 #FFF, 24px 36px 0 #a5a5a5, 28px 36px 0 #a5a5a5, 32px 36px 0 #a5a5a5, 36px 36px 0 #a5a5a5, 40px 36px 0 #000, 8px 40px 0 #000, 12px 40px 0 #000, 16px 40px 0 #a5a5a5, 20px 40px 0 #a5a5a5, 24px 40px 0 #a5a5a5, 28px 40px 0 #a5a5a5, 32px 40px 0 #000, 36px 40px 0 #000, 16px 44px 0 #000, 20px 44px 0 #000, 24px 44px 0 #000, 28px 44px 0 #000;
    }
    .pokeball#ultra {
        animation-delay: 0.5s;
        margin: -4px 0 0 108px;
        box-shadow: 16px 0 0 #000, 20px 0 0 #000, 24px 0 0 #000, 28px 0 0 #000, 8px 4px 0 #000, 12px 4px 0 #000, 16px 4px 0 #ffff00, 20px 4px 0 #ffff00, 24px 4px 0 #ffff00, 28px 4px 0 #ffff00, 32px 4px 0 #000, 36px 4px 0 #000, 4px 8px 0 #000, 8px 8px 0 #ffff00, 12px 8px 0 #ffff00, 16px 8px 0 #ffff00, 20px 8px 0 #ffff00, 24px 8px 0 #ffff00, 28px 8px 0 #ffff00, 32px 8px 0 #ffff00, 36px 8px 0 #ffff00, 40px 8px 0 #000, 4px 12px 0 #000, 8px 12px 0 #ffff00, 12px 12px 0 #ffff00, 16px 12px 0 #000, 20px 12px 0 #000, 24px 12px 0 #000, 28px 12px 0 #000, 32px 12px 0 #ffff00, 36px 12px 0 #ffff00, 40px 12px 0 #000, 0px 16px 0 #000, 4px 16px 0 #000, 8px 16px 0 #ffff00, 12px 16px 0 #ffff00, 16px 16px 0 #000, 20px 16px 0 #000, 24px 16px 0 #000, 28px 16px 0 #000, 32px 16px 0 #ffff00, 36px 16px 0 #ffff00, 40px 16px 0 #000, 44px 16px 0 #000, 0px 20px 0 #000, 4px 20px 0 #000, 8px 20px 0 #000, 12px 20px 0 #000, 16px 20px 0 #000, 20px 20px 0 #000, 24px 20px 0 #000, 28px 20px 0 #000, 32px 20px 0 #000, 36px 20px 0 #000, 40px 20px 0 #000, 44px 20px 0 #000, 0px 24px 0 #000, 4px 24px 0 #000, 8px 24px 0 #000, 12px 24px 0 #000, 16px 24px 0 #000, 20px 24px 0 #FFF, 24px 24px 0 #a5a5a5, 28px 24px 0 #000, 32px 24px 0 #000, 36px 24px 0 #000, 40px 24px 0 #000, 44px 24px 0 #000, 0px 28px 0 #000, 4px 28px 0 #FFF, 8px 28px 0 #000, 12px 28px 0 #000, 16px 28px 0 #000, 20px 28px 0 #a5a5a5, 24px 28px 0 #a5a5a5, 28px 28px 0 #000, 32px 28px 0 #000, 36px 28px 0 #000, 40px 28px 0 #a5a5a5, 44px 28px 0 #000, 4px 32px 0 #000, 8px 32px 0 #FFF, 12px 32px 0 #FFF, 16px 32px 0 #FFF, 20px 32px 0 #000, 24px 32px 0 #000, 28px 32px 0 #a5a5a5, 32px 32px 0 #a5a5a5, 36px 32px 0 #a5a5a5, 40px 32px 0 #000, 4px 36px 0 #000, 8px 36px 0 #a5a5a5, 12px 36px 0 #FFF, 16px 36px 0 #FFF, 20px 36px 0 #FFF, 24px 36px 0 #a5a5a5, 28px 36px 0 #a5a5a5, 32px 36px 0 #a5a5a5, 36px 36px 0 #a5a5a5, 40px 36px 0 #000, 8px 40px 0 #000, 12px 40px 0 #000, 16px 40px 0 #a5a5a5, 20px 40px 0 #a5a5a5, 24px 40px 0 #a5a5a5, 28px 40px 0 #a5a5a5, 32px 40px 0 #000, 36px 40px 0 #000, 16px 44px 0 #000, 20px 44px 0 #000, 24px 44px 0 #000, 28px 44px 0 #000;
    }
    .pokeball#master {
        animation-delay: 0.75s;
        margin: -4px 0 0 162px;
        box-shadow: 16px 0 0 #000, 20px 0 0 #000, 24px 0 0 #000, 28px 0 0 #000, 8px 4px 0 #000, 12px 4px 0 #000, 16px 4px 0 #481a66, 20px 4px 0 #481a66, 24px 4px 0 #481a66, 28px 4px 0 #481a66, 32px 4px 0 #000, 36px 4px 0 #000, 4px 8px 0 #000, 8px 8px 0 #eb23aa, 12px 8px 0 #eb23aa, 16px 8px 0 #481a66, 20px 8px 0 #481a66, 24px 8px 0 #481a66, 28px 8px 0 #481a66, 32px 8px 0 #eb23aa, 36px 8px 0 #eb23aa, 40px 8px 0 #000, 4px 12px 0 #000, 8px 12px 0 #eb23aa, 12px 12px 0 #FFF, 16px 12px 0 #FFF, 20px 12px 0 #481a66, 24px 12px 0 #481a66, 28px 12px 0 #FFF, 32px 12px 0 #FFF, 36px 12px 0 #eb23aa, 40px 12px 0 #000, 0px 16px 0 #000, 4px 16px 0 #481a66, 8px 16px 0 #481a66, 12px 16px 0 #FFF, 16px 16px 0 #481a66, 20px 16px 0 #FFF, 24px 16px 0 #FFF, 28px 16px 0 #481a66, 32px 16px 0 #FFF, 36px 16px 0 #481a66, 40px 16px 0 #481a66, 44px 16px 0 #000, 0px 20px 0 #000, 4px 20px 0 #481a66, 8px 20px 0 #481a66, 12px 20px 0 #481a66, 16px 20px 0 #481a66, 20px 20px 0 #000, 24px 20px 0 #000, 28px 20px 0 #481a66, 32px 20px 0 #481a66, 36px 20px 0 #481a66, 40px 20px 0 #481a66, 44px 20px 0 #000, 0px 24px 0 #000, 4px 24px 0 #000, 8px 24px 0 #481a66, 12px 24px 0 #481a66, 16px 24px 0 #000, 20px 24px 0 #FFF, 24px 24px 0 #a5a5a5, 28px 24px 0 #000, 32px 24px 0 #481a66, 36px 24px 0 #481a66, 40px 24px 0 #000, 44px 24px 0 #000, 0px 28px 0 #000, 4px 28px 0 #FFF, 8px 28px 0 #000, 12px 28px 0 #000, 16px 28px 0 #000, 20px 28px 0 #a5a5a5, 24px 28px 0 #a5a5a5, 28px 28px 0 #000, 32px 28px 0 #000, 36px 28px 0 #000, 40px 28px 0 #a5a5a5, 44px 28px 0 #000, 4px 32px 0 #000, 8px 32px 0 #FFF, 12px 32px 0 #FFF, 16px 32px 0 #FFF, 20px 32px 0 #000, 24px 32px 0 #000, 28px 32px 0 #a5a5a5, 32px 32px 0 #a5a5a5, 36px 32px 0 #a5a5a5, 40px 32px 0 #000, 4px 36px 0 #000, 8px 36px 0 #a5a5a5, 12px 36px 0 #FFF, 16px 36px 0 #FFF, 20px 36px 0 #FFF, 24px 36px 0 #a5a5a5, 28px 36px 0 #a5a5a5, 32px 36px 0 #a5a5a5, 36px 36px 0 #a5a5a5, 40px 36px 0 #000, 8px 40px 0 #000, 12px 40px 0 #000, 16px 40px 0 #a5a5a5, 20px 40px 0 #a5a5a5, 24px 40px 0 #a5a5a5, 28px 40px 0 #a5a5a5, 32px 40px 0 #000, 36px 40px 0 #000, 16px 44px 0 #000, 20px 44px 0 #000, 24px 44px 0 #000, 28px 44px 0 #000;
    }
    .pokeball#safari {
        animation-delay: 1s;
        margin: -4px 0 0 216px;
        box-shadow: 16px 0 0 #000, 20px 0 0 #000, 24px 0 0 #000, 28px 0 0 #000, 8px 4px 0 #000, 12px 4px 0 #000, 16px 4px 0 #9a4a01, 20px 4px 0 #9a4a01, 24px 4px 0 #606700, 28px 4px 0 #5fa300, 32px 4px 0 #000, 36px 4px 0 #000, 4px 8px 0 #000, 8px 8px 0 #606700, 12px 8px 0 #606700, 16px 8px 0 #606700, 20px 8px 0 #9a4a01, 24px 8px 0 #9a4a01, 28px 8px 0 #5fa300, 32px 8px 0 #606700, 36px 8px 0 #9a4a01, 40px 8px 0 #000, 4px 12px 0 #000, 8px 12px 0 #9a4a01, 12px 12px 0 #9a4a01, 16px 12px 0 #9a4a01, 20px 12px 0 #9a4a01, 24px 12px 0 #9a4a01, 28px 12px 0 #5fa300, 32px 12px 0 #606700, 36px 12px 0 #606700, 40px 12px 0 #000, 0px 16px 0 #000, 4px 16px 0 #5fa300, 8px 16px 0 #606700, 12px 16px 0 #5fa300, 16px 16px 0 #5fa300, 20px 16px 0 #606700, 24px 16px 0 #606700, 28px 16px 0 #606700, 32px 16px 0 #5fa300, 36px 16px 0 #9a4a01, 40px 16px 0 #9a4a01, 44px 16px 0 #000, 0px 20px 0 #000, 4px 20px 0 #5fa300, 8px 20px 0 #606700, 12px 20px 0 #5fa300, 16px 20px 0 #606700, 20px 20px 0 #000, 24px 20px 0 #000, 28px 20px 0 #606700, 32px 20px 0 #606700, 36px 20px 0 #5fa300, 40px 20px 0 #5fa300, 44px 20px 0 #000, 0px 24px 0 #000, 4px 24px 0 #000, 8px 24px 0 #606700, 12px 24px 0 #606700, 16px 24px 0 #000, 20px 24px 0 #FFF, 24px 24px 0 #a5a5a5, 28px 24px 0 #000, 32px 24px 0 #9a4a01, 36px 24px 0 #9a4a01, 40px 24px 0 #000, 44px 24px 0 #000, 0px 28px 0 #000, 4px 28px 0 #FFF, 8px 28px 0 #000, 12px 28px 0 #000, 16px 28px 0 #000, 20px 28px 0 #a5a5a5, 24px 28px 0 #a5a5a5, 28px 28px 0 #000, 32px 28px 0 #000, 36px 28px 0 #000, 40px 28px 0 #a5a5a5, 44px 28px 0 #000, 4px 32px 0 #000, 8px 32px 0 #FFF, 12px 32px 0 #FFF, 16px 32px 0 #FFF, 20px 32px 0 #000, 24px 32px 0 #000, 28px 32px 0 #a5a5a5, 32px 32px 0 #a5a5a5, 36px 32px 0 #a5a5a5, 40px 32px 0 #000, 4px 36px 0 #000, 8px 36px 0 #a5a5a5, 12px 36px 0 #FFF, 16px 36px 0 #FFF, 20px 36px 0 #FFF, 24px 36px 0 #a5a5a5, 28px 36px 0 #a5a5a5, 32px 36px 0 #a5a5a5, 36px 36px 0 #a5a5a5, 40px 36px 0 #000, 8px 40px 0 #000, 12px 40px 0 #000, 16px 40px 0 #a5a5a5, 20px 40px 0 #a5a5a5, 24px 40px 0 #a5a5a5, 28px 40px 0 #a5a5a5, 32px 40px 0 #000, 36px 40px 0 #000, 16px 44px 0 #000, 20px 44px 0 #000, 24px 44px 0 #000, 28px 44px 0 #000;
    }
</style>
