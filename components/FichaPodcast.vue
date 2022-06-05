<template>
<article id="ficha">
    <img src="/actualidad-imagen.png" alt="">
    <h1>Julia en la Onda</h1>
    <p>Toda la actualidad del momento con Julia Otero.</p>
    <boton-compuesto/>
</article>
</template>
<style lang="postcss" scoped>
#ficha{
    width: 30%;
    display: flex;
    flex-direction: column;
    margin: 0 50px 0 0;
    align-items: center;
}
img{
    width: 100%;
    margin: 0;
}

h1{
    width: 90%;
    margin: 15px 5% 5px 5%;
    font-size: 24px;
    font-family: sans-serif;
    font-weight: bold;
}
p{
    width: 90%;
    margin: 0 5% 30px 5%;
    font-size: 16px;
    color: #4f4f4f
}
</style>