<template>
  <section>
    <cabecera-desktop/>
    <main>
    <h1 class="bienvenida">Buenas tardes</h1>
    <flickity  class="flickity" ref="flickity" :options="flickityOptions">
     <card-vert-g 
      v-for="(item, index) in cardsv" 
      :key="index" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion" 
      class="carousel-cell"/>
    </flickity>
    
    <div class="c-horizontales">
        <card-hor 
      v-for="(item, i) in cardsh" 
      :key="i" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion" />
    </div>
      </main>
      <NavBar/>
  </section>
  
</template>

<script>
import Flickity from 'vue-flickity'
import CardEpi from '../components/CardEpi.vue'
export default {
  name: 'IndexPage',
  components: {
    Flickity,
    CardEpi
},
  data() {
    return {
      flickityOptions: {
        initialIndex: 3,
        freeScroll: true,
        contain: true,
        prevNextButtons: false,
        pageDots: false
        // any options from Flickity can be used
      },
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
        },
        {
          
          titulo: 'La Parroquia',
          descripcion: 'cuarta',
          source: '/humor_imagen.png'
        },
        {
          
          titulo: 'La Parroquia',
          descripcion: 'cuarta',
          source: '/humor_imagen.png'
        },
        ],
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
        
    }
  }
  }
</script>
<style lang="postcss" scoped>
*{
  box-sizing: border-box;
}
.bienvenida{
  font-weight: bold;
  color: #95C11F;
  font-size: 24px;
  margin-bottom: 30px;
  padding-top: 30px;
}

.c-horizontales{
  margin: 40px 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  flex-wrap: wrap;
}
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
        section{
          background-color: #f5f5f5;
        }

        main{
          margin-top: 100px;
          padding: 0 30px 30px 30px;
        }
        </style>