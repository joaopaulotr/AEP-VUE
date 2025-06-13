<template>
  <div id="app">
    <!-- Header -->
    <HeaderComponent />
    
    <!-- Seção Introdução -->
    <IntroducaoComponent />
    
    <!-- Seção Objetivo -->
    <ObjetivoComponent />
    
    <!-- Seção Metodologia -->
    <MetodologiaComponent />
    
    <!-- Seção Resultados Esperados -->
    <ResultadosComponent />
    
    <!-- Formulário de Denúncia -->
    <FormularioDenunciaComponent />
    
    <!-- Seção Considerações Finais -->
    <ConsideracoesFinaisComponent />
    
    <!-- Footer -->
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import IntroducaoComponent from './components/IntroducaoComponent.vue'
import ObjetivoComponent from './components/ObjetivoComponent.vue'
import MetodologiaComponent from './components/MetodologiaComponent.vue'
import ResultadosComponent from './components/ResultadosComponent.vue'
import FormularioDenunciaComponent from './components/FormularioDenunciaComponent.vue'
import ConsideracoesFinaisComponent from './components/ConsideracoesFinaisComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    IntroducaoComponent,
    ObjetivoComponent,
    MetodologiaComponent,
    ResultadosComponent,
    FormularioDenunciaComponent,
    ConsideracoesFinaisComponent,
    FooterComponent
  }
}
</script>

<style>
/* Estilos específicos do App, se necessário */
#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>

