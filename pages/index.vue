<template>
  <section>
    <h1>Buenas tardes</h1>
    <div>
    <card-vert-g 
      v-for="item in cardsv" 
      :key="i" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion" />
      </div>
      <div>
        <card-hor 
      v-for="item in cardsh" 
      :key="i" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion" />
      </div>
      <div>
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
      />
      </div>
  </section>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      cardsv: [
        {
          titulo: 'Julia en la Onda',
          descripcion: 'Una descripcion',
          source: '/actualidad-imagen.png'
        },
        {
          titulo: 'Más de uno',
          descripcion: 'segunda des',
          source: '/cultura_imagen.png'
        },
        {
          titulo: 'Botón 3',
          descripcion: 'tercera',
          source: '/deporte_imagen.png'
        },
        {
          titulo: 'La Parroquia',
          descripcion: 'cuarta',
          source: '/humor_imagen.png'
        }],
        cardsh: [
        {
          titulo: 'Julia en la Onda',
          descripcion: 'Una descripcion',
          source: '/actualidad-imagen.png'
        },
        {
          titulo: 'Más de uno',
          descripcion: 'segunda des',
          source: '/cultura_imagen.png'
        },
        {
          titulo: 'Botón 3',
          descripcion: 'tercera',
          source: '/deporte_imagen.png'
        },
        {
          titulo: 'La Parroquia',
          descripcion: 'cuarta',
          source: '/humor_imagen.png'
        }],
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
<style lang="postcss">
h2{
            color: black;
            font-size: 24px;
            font-weight: bold;
        }
        p{
            color: #4f4f4f;
            font-size: 16px;
        }
        h3{
          color: black;
            font-size: 20px;
            font-weight: bold;
        }
        </style>