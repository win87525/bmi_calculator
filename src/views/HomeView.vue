<template>
  <main>
    <hero></hero>
    <result></result>
    <tips></tips>
  </main>
</template>

<script setup>
import hero from '@/components/hero/hero.vue';
import result from '@/components/result.vue';
import tips from '@/components/tips.vue';
</script>
<style scoped>
main{
  display: grid;
  grid-template-columns: 1fr;
  gap: 10rem;
}
</style>
