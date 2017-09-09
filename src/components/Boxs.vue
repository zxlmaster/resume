<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container">
        <h2 class="btn subtitle"> {{ title }} </h2>
        <box v-for="item in list"
          :key="item.name"
          :content="item"></box>
      </div>
    </div>
  </section>
</template>

<script>
import Box from '@/components/Box';

export default {
  name: 'Boxs',
  props: {
    list: Array,
    title: String,
  },
  components: {
    box: Box,
  },
};
</script>

<style scoped>
</style>
