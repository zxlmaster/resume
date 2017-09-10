<template>
  <div class="resume-tags tags field is-grouped columns is-centered">
    <tag v-for="(item, index) in tags"
      :key="index"
      :title="item.title"
      :icon="item.icon"
      :content="item.content"
      :colour="colour"></tag>
  </div>
</template>

<script>
import Tag from '@/components/Tag';

export default {
  name: 'Tags',
  props: {
    tags: Object,
    colour: String,
  },
  components: {
    tag: Tag,
  },
};
</script>

<style scoped>
.resume-tags {
  margin-bottom: 25px;
}
</style>

