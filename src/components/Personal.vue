<template>
  <section class="hero is-primary is-bold">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">{{ user.username }}</h1>
        <h2 class="subtitle">{{ user.profession }}</h2>
        <tags :tags="user.school" colour="success"></tags>
        <tags :tags="user.social"></tags>
      </div>
    </div>
  </section>
</template>

<script>
import Tags from '@/components/Tags';

export default {
  name: 'Personal',
  props: {
    user: Object,
  },
  components: {
    tags: Tags,
  },
};
</script>
