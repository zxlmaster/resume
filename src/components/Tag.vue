<template>
  <div class="control">
    <div class="tags has-addons">
      <span class="tag">
        <icon v-if="icon" size="small" :icon="icon"></icon>
        <span v-else>{{ title }}</span>
      </span>
      <span :class="contentClass">{{ content }}</span>
    </div>
  </div>
</template>

<script>
import Icon from '@/components/Icon';

export default {
  name: 'SocialTags',
  props: {
    title: String,
    icon: String,
    content: String,
    colour: String,
  },
  components: {
    icon: Icon,
  },
  computed: {
    contentClass() {
      return this.colour
        ? `tag is-${this.colour}`
        : 'tag is-info';
    },
  },
};
</script>
