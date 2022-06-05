<template> 
    <button>
        <img 
            :src="isPlaying? '/pause.svg':'/play_verde.svg'" 
            alt="Botón play" 
            class="btn-play" />
    </button>
     
</template>


<script>
export default{
    props: ['isPlaying']
}
</script>

<style lang="postcss" scoped>
img{
    min-width: 35px;
    height: 35px;
}
</style>