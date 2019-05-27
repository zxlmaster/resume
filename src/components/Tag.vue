<template>
  <div class="control">
    <a :href="href ? href: 'javascript:void(0);'">
      <div class="tags has-addons is-mobile-margin">
        <span class="tag">
          <icon v-if="icon" size="small" :icon="icon"></icon>
          <span v-else>{{ title }}</span>
        </span>

        <span :class="contentClass">{{ content }}</span>
      </div>
    </a>
  </div>
</template>

<script>
import Icon from "@/components/Icon";

export default {
  name: "SocialTags",
  props: {
    title: String,
    icon: String,
    content: String,
    colour: String,
    href: String
  },
  components: {
    icon: Icon
  },
  computed: {
    contentClass() {
      return this.colour ? `tag is-${this.colour}` : "tag is-info";
    }
  }
};
</script>

<style scoped>
@media screen and (max-width: 768px) {
  .is-mobile-margin {
    margin-top: 10px;
  }
}
</style>
