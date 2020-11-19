<template>
  <div class="title-section-container">
      <div class="content">
          <div v-if="topSpacing" class="TopSpacing"/>
          <h2>{{title}}</h2>
          <div class="divider" />
          <p>
              {{description}}
          </p>
      </div>
  </div>
</template>

<script>

export default {
    name: 'TitleSection',
    props: {
        topSpacing: Boolean,
        title: String,
        description: String
    }
}
</script>
