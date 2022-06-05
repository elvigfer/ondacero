<template>
<div class="container">
         <img v-if="source" :src="source" :alt="alt" class="portada">
         <img src="/opciones.svg" alt="Botón opciones" class="btn-opciones">
         <div class="card-texto">
            <h4><span class="dato">{{numero}}</span>  {{titulo}}</h4>
            <p>{{descripcion}}</p>
            <p class="dato">{{fecha}} • {{duracion}}</p>
         </div>
         <button @click="playpause">
          <boton-play :isPlaying="isPlaying" /></button>
          <!--<BotonPause v-show="isPlaying"/>-->
          
         </div>
</template>
<script>
import {Howl, Howler} from 'howler';
export default{
    props: ['source', 'alt', 'numero', 'titulo', 'descripcion', 'fecha', 'duracion'],
    data(){
        return{
            sound: '',
            isPlaying: false
        }
    },
    mounted(){
        this.sound = new Howl({
      src: ['/audios/trouble.mp3']
    });
    },
    methods: {
        playpause(){
            if(this.sound.playing()){
                this.sound.pause();
                this.isPlaying = false;
            } else{this.sound.play();
                this.isPlaying= true;}
        }
    }
}
</script>
<style lang="postcss" scoped>
.container {
  width: 95%;
  height: 100px;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  margin-right: 30px;
  border-bottom: 1pt solid #C4C4C4;
  }

  h4{
    font-family: sans-serif;
    font-weight: bold;
    font-size: 16px;
    margin: 0;
    }
    .dato {
      font-family: sans-serif;
      color: #373737;
      }
  .portada{
    width: 100px;
    }
  .dato{
    font-family: sans-serif;
    font-weight: lighter;
    color: #373737;
    font-size: 14px;
    }
    .btn-opciones{
        width: 40px;
    }
  .card-texto{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    height: 60px;
    border: none;
    margin: 0;
    width: 75%;
  }
</style>
