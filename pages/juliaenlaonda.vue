<template>
<main>
  <section>
  <ficha-podcast/>
  <article>
    <h2 id="epi">Episodios</h2>
    <div class="scroll">
    <card-epi 
      v-for="item in cardse" 
      :key="i" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion"
      :numero="item.numero"
      :fecha="item.fecha"
      :duracion="item.duracion"
      /></div></article>
      </section>
      <nav-bar/>
</main>

</template>
<script>
export default {
  name: 'detalle',
  data() {
    return {
        cardse: [
        {
          titulo: 'Julia en la Onda',
          descripcion: 'Una descripcion',
          source: '/actualidad-imagen.png',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Más de uno',
          descripcion: 'segunda des',
          source: '/cultura_imagen.png',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Botón 3',
          descripcion: 'tercera',
          source: '/deporte_imagen.png',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'La Parroquia',
          descripcion: 'cuarta',
          source: '/humor_imagen.png',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        }],
    }
  }
}
</script>

<style lang="postcss" scoped>
article{
  width: 65%;
}
#epi{
  font-size: 32px;
  font-weight: bold;
  position: fixed;
}
section{
  display: flex;
  flex-direction: row;
  padding: 30px;
}
.scroll{
  margin-top: 60px;
}
</style>