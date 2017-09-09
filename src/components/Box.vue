<template>
  <div class="resume-box">
    <h3>{{content.name}}</h3>
    <p v-if="showTime" class="time">{{ time }}</p>
    <ul v-for="desc in content.description">
      <li>{{ desc }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Box',
  props: {
    content: Object,
  },
  computed: {
    showTime() {
      return this.content.time !== undefined;
    },
    time() {
      const start = this.content.time.start;
      const end = this.content.time.end;

      return `${start} 至 ${end}`;
    },
  },
};
</script>

<style scoped>
  .resume-box {
    margin-bottom: 25px;
  }
  .resume-box li {
    color: #999;
  }
</style>
