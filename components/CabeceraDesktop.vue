<template>
<div id="cabecera">
    <nav>
        <img class="perfil" src="/Avatar.svg" alt="">
        <ul class="menu-superior">
           <NuxtLink to="/"><li>Incio</li></NuxtLink> 
            <NuxtLink to="/vacio"><li>Mis colecciones</li></NuxtLink>
            <NuxtLink to="/vacio"><li>Buscador</li></NuxtLink>
            <NuxtLink to="/vacio"><li>Ajustes</li></NuxtLink>
        </ul>
    </nav>
    <NuxtLink to="/"><img src="/logo.svg" alt="logo onda cero"></NuxtLink>
</div>
</template>
<style lang="postcss" scoped>
#cabecera{
    width: 100%;
    height: 100px;
    background-color: white;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 0 20px;
    align-items: center;
    position: fixed;
    top: 0;
    box-shadow: 2px 2px 7px rgb(168, 168, 168);
    z-index: 9999;
}
nav{
    width: 400px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
ul{
    width: 320px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-weight: bold;
}
li:hover{
    color: #95C11F;
}
@media (max-width: 600px){
    ul{
        display: none;
    }
}
</style>