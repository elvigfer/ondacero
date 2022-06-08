<template>
<div class="c-horizontal">
    <NuxtLink :to="{name: 'programas-programa', params: {titulo: titulo}}">
        <img :src="source" :alt="alt" class="portada">
        <div class="card-texto">
            <h3>{{titulo}}</h3>
            <p>{{descripcion}}</p>
        </div></NuxtLink>
        <button @click="playpause">
        <BotonPlay  :isPlaying="isPlaying" /></button>
</div>
</template>
<script>
import {Howl, Howler} from 'howler';
export default{
    props: ['link', 'source', 'alt', 'titulo', 'descripcion'],
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
    h3{
        font-weight: bold;
        font-size: 20px;
    }
    p{
        font-size: 16px;
        color: #414141;
    }
    .c-horizontal{
        width: 100%;
        min-width: 300px;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        height: 100px;
        border-top-right-radius: 50px;
        border-bottom-right-radius: 50px;
        background-color: white;
        box-shadow: 2px 2px 4px lightgray;
        max-width: 380px;
        margin-right: 10px;
         margin-bottom: 15px;
    }
    .portada{
        height: 100px;
    }
    .card-texto{
        width: 70%;
        margin-left: 15px;
        margin-right: 10px;
    }
    button{
        width: 30px;
        height: 30px;
        margin-right: 10px;
        .btn-play{
        width: 30px;
    }
    }
    a{
        display: flex;
        flex-direction: row;
    }
    
</style>