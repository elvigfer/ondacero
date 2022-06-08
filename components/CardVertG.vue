<template>
   <NuxtLink :to="{name: 'programas-programa', params: {titulo: titulo}}">
   <article>
        <img :src="source" :alt="titulo">
        <h2>{{titulo}}</h2>
        <p>{{descripcion}}</p>
    </article></NuxtLink>
</template>

<script>
export default{
    props: ['source', 'titulo', 'descripcion']
}
</script>

<style lang="postcss" scoped>
article{
    margin: 0;
        width: 200px;
        img{
            width: 90%;
            object-fit: cover;
        }
        h2, p{
            padding-left: 10px;
        }
        h2{
            font-weight: bold;
            font-size: 20px;
        }
}
        
</style>
