<template>
<div class="c-horizontal">
        <img :src="source" :alt="alt" class="portada">
        <div class="card-texto">
            <h3>{{titulo}}</h3>
            <p>{{descripcion}}</p>
        </div>
        <button><img src="/play_verde.svg" alt="Botón play" class="btn-play"></button> 
</div>
</template>
<script>
export default{
    props: ['source', 'alt', 'titulo', 'descripcion']
}
</script>
<style lang="postcss" scoped>
    .c-horizontal{
        width: 90%;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        height: 100px;
        border-top-right-radius: 50px;
        border-bottom-right-radius: 50px;
        background-color: white;
        box-shadow: 2px 2px 4px lightgray;
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