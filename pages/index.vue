<template>
  <section>
    <cabecera-desktop/>
    <main>
    <h1 class="bienvenida">Buenas tardes</h1>
    <h2>Especialmente para ti</h2>
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
    <h2>Actualidad</h2>
    <div class="c-horizontales">
        <card-hor 
      v-for="(item, i) in cardsh" 
      :key="i" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion" />
    </div>
    <h2>Cultura y humor</h2>
    <flickity  class="flickity ultimo" ref="flickity" :options="flickityOptions">
     <card-vert-g 
      v-for="(item, index) in cardsvdos" 
      :key="index" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion" 
      class="carousel-cell"/>
    </flickity>
    <reproductor />
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
        
      },
      cardsv: [
        {
          
          titulo: 'Julia en la Onda',
          descripcion: 'La actualidad con Julia Otero',
          source: '/actualidad-imagen.png'
        },
        {
          
          titulo: 'Más de uno',
          descripcion: 'El programa matinal de Carlos Alsina',
          source: '/cultura_imagen.png'
        },
        {
          
          titulo: 'After Hours',
          descripcion: 'Con Gemma Ruiz e Isa Blanco',
          source: '/after.png'
        },
        {
          
          titulo: 'La Parroquia',
          descripcion: 'Todo el humor con El Monaguillo',
          source: '/humor_imagen.png'
        },
        {
          
          titulo: 'La Cultureta',
          descripcion: 'La tertulia de Rubén Amón',
          source: '/cultureta.png'
        },
        {
          
          titulo: 'Radioestadio',
          descripcion: 'Información deportiva con Edu García',
          source: '/deporte_imagen.png'
        },
        
        ],
        cardsh: [
        {
          titulo: 'Por fin no es lunes',
          descripcion: 'Entrevistas con Jaime Cantizano',
          source: '/lunes.png'
        },
        {
          titulo: 'Noticias mediodía',
          descripcion: 'Actualidad de la mano de Elena Gijón',
          source: '/noticias.png'
        },
        {
          titulo: 'No son horas',
          descripcion: 'El programa nocturno de José Luis Salas',
          source: '/nohoras.png'
        }],
        cardsvdos: [
        {
          
          titulo: '1931',
          descripcion: 'Viajamos al 1931 y la II República',
          source: '/1931.png'
        },
        {
          
          titulo: 'Toma la pastilla roja',
          descripcion: 'Ciencia ficción y cine',
          source: '/pastilla.jpg'
        },
        {
          
          titulo: 'Kinótico',
          descripcion: 'Cine, series y cultura',
          source: '/deporte_imagen.png'
        },
        {
          
          titulo: 'La Parroquia',
          descripcion: 'Todo el humor con El Monaguillo',
          source: '/humor_imagen.png'
        },
        {
          
          titulo: 'Rock&Roll Animal',
          descripcion: 'cuarta',
          source: '/rock.jpg'
        },
        {
          
          titulo: '¡Cállate, payaso!',
          descripcion: 'cuarta',
          source: '/payaso.png'
        },
        ],
    }
  }
  }
</script>
<style lang="postcss" scoped>
.flickity{
  margin-bottom: 20px;
  padding: 0;
  width: 100%;
}
*{
  box-sizing: border-box;
}
.bienvenida{
  font-weight: bold;
  color: #95C11F;
  font-size: 24px;
  margin-left: 30px;
  margin-bottom: 30px;
  padding-top: 30px;
}
h2{
  margin-bottom: 20px;
}
.c-horizontales{
  margin: 30px;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  flex-wrap: wrap;
}
h2{
            color: black;
            font-size: 24px;
            font-weight: bold;
            margin-left: 30px;
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
          margin-top: 80px;
          padding: 0;
        }
        .ultimo{
          margin-bottom: 180px;
          padding-bottom: 20px;
        }
        .flickity{
          padding-left: 15px;
        }
        @media (max-width: 600px){
          .ultimo{
          margin-bottom: 265px;
          padding-bottom: 20px;
        }
        }
        </style>