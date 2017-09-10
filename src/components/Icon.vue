<template>
  <span :class="sizeClass">
    <i :class="iconClass"></i>
  </span>
</template>

<script>
export default {
  name: 'SocialTags',
  props: {
    size: String,
    icon: String,
  },
  computed: {
    sizeClass() {
      return this.size ? `icon is-${this.size}` : 'icon';
    },
    iconClass() {
      return this.icon ? `fa fa-${this.icon}` : 'fa';
    },
  },
};
</script>
