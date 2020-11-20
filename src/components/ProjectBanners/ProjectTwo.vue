<template>
  <div class="project-banner-two-container">
      <div class="content">
        <img :src="imgLogo" />
        <div class="divider" />
        <h2>{{title}}</h2>
        <p>
          {{description}}
        </p>
        <div class="tags">
          <img :src="imgTag" />
          <a v-for="tag in tags.data" v-bind:key="tag.id" href="#">{{tag.descripcion}}</a>
        </div>
        <button>
          Ver Detalles
        </button>
      </div>
      <img :src="img" />
  </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'ProjectTwo',
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
      .get('http://localhost/api.php?accion=mostrar-tags&id-proyecto=2') /*data de tags filtrado por el id del proyecto destacado*/
      .then(response => (this.tags = response)) 
  }
}
</script>
