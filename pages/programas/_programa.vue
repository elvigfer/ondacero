<template>
<main>
    <cabecera-desktop/>
  <section class="cuerpo">
  <!--<ficha-podcast/>-->
  <article id="ficha">
    <img :src="program.source" alt="">
    <h1>{{program.titulo}}</h1>
    <p>{{program.descripcion}}</p>
    <boton-compuesto/>
</article>
  <article class="episodios">
    <h2 id="epi">Episodios</h2>
    <div class="scroll">
    <card-epi 
      v-for="item in program.episodios" 
      :key="i" 
      :source="item.source" 
      :alt="item.titulo" 
      :titulo="item.titulo"
      :descripcion="item.descripcion"
      :numero="item.numero"
      :fecha="item.fecha"
      :duracion="item.duracion"
      />
      </div></article>
      </section>
      <nav-bar/>
</main>

</template>

<script>
export default {


    computed: {
        // a computed getter
        program() {
        // `this` points to the component instance
            return this.cards.find(
                (el) => el.titulo === this.$route.params.titulo
            )
        }
    },
    data() {
        return {
            cards: [
                {

                    titulo: 'Julia en la Onda',
                    descripcion: 'La actualidad con Julia Otero',
                    source: '/actualidad-imagen.png',
                    episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
                },
                {
          
          titulo: 'Más de uno',
          descripcion: 'El programa matinal de Carlos Alsina',
          source: '/cultura_imagen.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'After Hours',
          descripcion: 'Con Gemma Ruiz e Isa Blanco',
          source: '/after.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'La Parroquia',
          descripcion: 'Todo el humor con El Monaguillo',
          source: '/humor_imagen.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'La Cultureta',
          descripcion: 'La tertulia de Rubén Amón',
          source: '/cultureta.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'Radioestadio',
          descripcion: 'Información deportiva con Edu García',
          source: '/deporte_imagen.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          titulo: 'Por fin no es lunes',
          descripcion: 'Entrevistas con Jaime Cantizano',
          source: '/lunes.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          titulo: 'Noticias mediodía',
          descripcion: 'Actualidad de la mano de Elena Gijón',
          source: '/noticias.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          titulo: 'No son horas',
          descripcion: 'El programa nocturno de José Luis Salas',
          source: '/nohoras.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: '1931',
          descripcion: 'Viajamos al 1931 y la II República',
          source: '/1931.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'Toma la pastilla roja',
          descripcion: 'Ciencia ficción y cine',
          source: '/pastilla.jpg',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'Kinótico',
          descripcion: 'Cine, series y cultura',
          source: '/deporte_imagen.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'La Parroquia',
          descripcion: 'Todo el humor con El Monaguillo',
          source: '/humor_imagen.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: 'Rock&Roll Animal',
          descripcion: 'cuarta',
          source: '/rock.jpg',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        },
        {
          
          titulo: '¡Cállate, payaso!',
          descripcion: 'cuarta',
          source: '/payaso.png',
          episodios: [
                        {
          titulo: 'Título del episodio',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 2',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 3',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Título del episodio 5',
          descripcion: 'Una descripción',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
        }
        ],
            
        }
    }
}
</script>

<style lang="postcss" scoped>
.cuerpo{
    margin-top: 100px;
}
#ficha{
  width: 30%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: sticky;
  h1{
      font-size: 30px;
      font-weight: bold;
      font-family: sans-serif;
  }
  p{
      font-size: 16px;
      margin: 10px 0 30px 0;
  }
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
  width: 100%;
}
.episodios{
  width: 90%;
  margin-left: 10%;
}
.scroll{
    margin-top: 60px;
}
section{
    background-color: #f5f5f5;
    height: 100%;
}

 @media (max-width: 600px){
     section{
         flex-direction: column;
     }
     #epi{
         position: relative;
     }
     .scroll{
         margin: 0 0 85px 0;
     }
     #ficha{
         width: 90%;
         margin-bottom: 20px;
         img{
             width: 60%;
         }
     }
 }
</style>