<template>
  <div class="resume">
    <personal :user="user"></personal>
    <boxs :title="experienceTitle" :list="experience"></boxs>
    <boxs :title="skillTitle" :list="experience"></boxs>
  </div>
</template>

<script>
import Personal from '@/components/Personal';
import Boxs from '@/components/Boxs';
import user from '@/database/personal';
import experience from '@/database/experience';

export default {
  components: {
    personal: Personal,
    boxs: Boxs,
  },
  data() {
    return {
      user,
      experience,
      experienceTitle: 'Experiences',
      skillTitle: 'Skills',
    };
  },
};
</script>
