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
  </div>
</template>

<script>
import MainBanner from './MainBanner/index';
import NewsBar from './NewsBar/index';
import TitleSection from './TitleSection/index';
import CardElement from './CardElement/index';

export default {
  name: 'HomePage',
  components: {
    MainBanner,
    NewsBar,
    TitleSection,
    CardElement
  }
}
</script>
