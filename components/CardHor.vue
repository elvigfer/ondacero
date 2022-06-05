<template>
<a :href="link"> <div class="c-horizontal">
        <img :src="source" :alt="alt" class="portada">
        <div class="card-texto">
            <h3>{{titulo}}</h3>
            <p>{{descripcion}}</p>
        </div>
        <button @click="playpause">
        <BotonPlay  :isPlaying="isPlaying" /></button>
</div></a>
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
    }
    .portada{
        height: 100px;
    }
    .card-texto{
        width: 70%;
        margin-left: 15px;
    }
    button{
        width: 30px;
        height: 30px;
        margin-right: 10px;
        .btn-play{
        width: 30px;
    }
    }
</style>