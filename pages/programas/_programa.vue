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
                    descripcion: 'Una descripcion',
                    source: '/actualidad-imagen.png',
                    episodios: [
                        {
          titulo: 'Julia en la Onda',
          descripcion: 'Una descripcion',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Más de uno',
          descripcion: 'segunda des',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'Botón 3',
          descripcion: 'tercera',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        {
          titulo: 'La Parroquia',
          descripcion: 'cuarta',
          source: '',
          numero: '00X00',
          fecha: '25/05/22',
          duracion: '51 min'
        },
        
                    ]
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
                    titulo: 'Julia en la Onda 2',
                    descripcion: 'Una descripcion 2',
                    source: '/actualidad-imagen.png'
                },
                {
                    titulo: 'Más de uno 2',
                    descripcion: 'segunda des 2',
                    source: '/cultura_imagen.png'
                },
                {
                    titulo: 'Botón 3 2',
                    descripcion: 'tercera 2',
                    source: '/deporte_imagen.png'
                },
                {
                    titulo: 'La Parroquia 2',
                    descripcion: 'cuarta 2',
                    source: '/humor_imagen.png'
                }],
            
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
}

</style>