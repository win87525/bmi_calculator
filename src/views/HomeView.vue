<template>
  <main>
    <hero></hero>
    <result></result>
    <tips></tips>
    <limitations></limitations>
    <test1></test1>
  </main>
</template>

<script setup>
import hero from '@/components/hero/hero.vue';
import result from '@/components/result.vue';
import tips from '@/components/tips.vue';
import limitations from '@/components/limitations.vue';
import test1 from '@/components/test1.vue';
</script>
<style scoped lang="scss">
main{
  display: grid;
  grid-template-columns: 1fr;
  gap: 10rem;
}
</style>
