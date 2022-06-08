<template>
<nav>
    <NuxtLink to="/"><button><img src="/home.svg" alt="Home"></button></NuxtLink>
    <NuxtLink to= "/vacio"><button><img src="/buscar_AF.svg" alt="Buscar"></button></NuxtLink>
    <NuxtLink to="/vacio"><button><img src="/biblioteca_AF.svg" alt="Colecciones"></button></NuxtLink>
    <NuxtLink to="/vacio"><button><img src="/ajustes_AF.svg" alt="Ajustes"></button></NuxtLink>
</nav>
</template>
<style lang="postcss" scoped>
nav{
    display: none;
}
@media (max-width: 600px){
nav{
    width: 100%;
    height: 85px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    background-color: black;
    position: fixed;
    bottom: 0;
}
button{
    width: 35px;
    height: 42px;
}
img{
    width: 35px;
}}
</style>