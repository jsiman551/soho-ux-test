<template>
  <div class="project-banner-three-container">
      <img :src="img" />
      <div class="content">
        <img :src="imgLogo" />
        <div class="divider" />
        <h2>{{title}}</h2>
        <p>
          {{description}}
        </p>
        <div class="tags">
          <img :src="imgTag" />
          <a v-for="tag in tags.data" v-bind:key="tag" href="#">{{tag.descripcion}}</a>
        </div>
        <button>
          Ver Detalles
        </button>
      </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'ProjectThree',
    props: {
        title: String,
        description: String,
        img: String,
        imgLogo: String,
        imgTag: String
    },  
  data () {
    return {
      tags: null
    }
  },
  mounted () {
    axios
      .get('http://localhost/api.php?accion=mostrar-tags&id-proyecto=3') /*data de tags filtrado por el id del proyecto destacado*/
      .then(response => (this.tags = response)) 
  }
}
</script>
