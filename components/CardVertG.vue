<template>
    <article>
        <img :src="source" :alt="titulo">
        <h2>{{titulo}}</h2>
        <p>{{descripcion}}</p>
    </article>
</template>

<script>
export default{
    props: ['source', 'titulo', 'descripcion']
}
</script>

<style lang="postcss" scoped>
article{
        width: 200px;
        img{
            width: 100%;
            object-fit: cover;
        }
        h2, p{
            padding-left: 10px;
        }
}
        
</style>
