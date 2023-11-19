<script setup>
import Header from '@/components/Header.vue';
import ContentHome from '@/components/ContentHome.vue';
import CarrouselVideo from '@/components/CarrouselVideo.vue';

</script>

<template>
  <div class="home">
  <Header text="Violência doméstica contra as mulheres trans: A concepção de violência doméstica e familiar da Lei Maria
    da Penha e o alcance trazido no texto normativo." />
  <CarrouselVideo /> 
  <ContentHome/>
  </div>
    
</template>

<style scoped>

.home{
    display: flex !important;
    flex-direction: column !important;
    width: 100%;
    min-height: 100vh;
}

</style>
