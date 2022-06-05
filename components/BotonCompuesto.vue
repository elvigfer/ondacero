<template>
<button ><div class="simple">Escuchar</div><div class="circular"><img  src="/play_negro.svg" alt=""></div></button>
</template>
<script>

</script>

<style lang="postcss" scoped>
    button{
    width: 180px;
    border: none;
    display: flex;
    flex-direction: row;
    }
    .simple{
        height: 40px;
        background-color: #95C11F;
        width: 140px;
        border-radius: 60px;
        font-size: 20px;
        font-weight: bold;
        padding-top: 3px;
    }
    .circular{
        height: 40px;
        width: 40px;
        background-color: #95C11F;
        border-radius: 50px;
        margin-left: -2px;
    }
    img{
        height: 28px;
        padding-left: 15px;
        padding-top: 10px;
    }
</style>