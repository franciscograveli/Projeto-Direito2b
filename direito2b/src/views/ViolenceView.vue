<script setup>
import ContentViolence from '@/components/ContentViolence.vue';
</script>
<template>
  <div class="violence">
    <ContentViolence/>
  </div>
</template>

<style>
.violence{
    display: flex !important;
    flex-direction: column !important;
    width: 100%;
    min-height: 100vh;
}
@media (min-width: 1024px) {
  .violence {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
