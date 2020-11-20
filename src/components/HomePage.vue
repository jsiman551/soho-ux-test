<template>
  <div>
    <MainBanner />
    <NewsBar />
    <TitleSection 
      title="17 años de experiencia en pos de tu proyecto" 
      description="Especializados desde 1996 en usabilidad, experiencia del usuario (UX) y diseño de experiencias 
                de proyectos digitales. Aportamos estrategia e innovación centrada en el usuario y los 
                objetivos de negocio de tu proyecto. Cotrabajando mejoraremos tu tasa de conversión,
                KPI's, ROI y los resultados de tu actual publicidad PPC (pay per click)."
    />
    <div class="cards-container">
      <CardElement
        title="Estrategia, Usabilidad & ux" 
        description="Te ofrecemos excelente usabilidad y 
        experiencia del usuario en tu proyecto, junto a una visión innovadora" 
      />
      <CardElement 
        title="Mejoramos la experiencia" 
        description="Tangibilizamos tu proyecto digital a través de un diseño centrado en el usuario
         y técnicas avanzadas" 
      />
      <CardElement 
        title="Medición continua de objetivos" 
        description="implementación, testing con usuarios y medición continua son necesarias para 
        garantizar el éxito de tu proyecto" 
      />
    </div>
    <TitleSection 
      topSpacing
      title="Proyectos destacados" 
      description="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
      ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, 
      nascetur ridiculus mus."
    />
    <ProjectOne 
      :title="proyectos.data[0].title" 
      :description="proyectos.data[0].description" 
      :img="proyectos.data[0].img" 
      :imgLogo="proyectos.data[0].imglogo" 
      :imgTag="proyectos.data[0].imgtag"
    />
    <ProjectTwo 
      :title="proyectos.data[1].title" 
      :description="proyectos.data[1].description" 
      :img="proyectos.data[1].img" 
      :imgLogo="proyectos.data[1].imglogo" 
      :imgTag="proyectos.data[1].imgtag" 
    />
    <ProjectThree 
      :title="proyectos.data[2].title" 
      :description="proyectos.data[2].description" 
      :img="proyectos.data[2].img" 
      :imgLogo="proyectos.data[2].imglogo" 
      :imgTag="proyectos.data[2].imgtag" 
    />
    <img class="footer-icon" src="/images/footer-logo.png">
    <Footer />
  </div>
</template>

<script>
import axios from 'axios'
import MainBanner from './MainBanner/index';
import NewsBar from './NewsBar/index';
import TitleSection from './TitleSection/index';
import CardElement from './CardElement/index';
import ProjectOne from './ProjectBanners/ProjectOne';
import ProjectTwo from './ProjectBanners/ProjectTwo';
import ProjectThree from './ProjectBanners/ProjectThree';
import Footer from './Footer/index';

export default {
  name: 'HomePage',
  components: {
    MainBanner,
    NewsBar,
    TitleSection,
    CardElement,
    ProjectOne,
    ProjectThree,
    ProjectTwo,
    Footer
  },
  data () {
    return {
      proyectos: null
    }
  },
  mounted () {
    axios
      .get('http://localhost/api.php?accion=mostrar-proyectos') /*proyectos destacados data*/
      .then(response => (this.proyectos = response))
  }
}
</script>
