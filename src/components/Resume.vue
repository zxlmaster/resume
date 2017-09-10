<template>
  <div class="resume">
    <personal :user="user"></personal>
    <boxs :title="experienceTitle" :list="experience"></boxs>
    <boxs :title="skillTitle" :list="skill"></boxs>
    <boxs :title="articleTitle" :list="article"></boxs>
    <boxs :title="codeTitle" :list="code"></boxs>
  </div>
</template>

<script>
import Personal from '@/components/Personal';
import Boxs from '@/components/Boxs';
import user from '@/database/personal';
import experience from '@/database/experience';
import skill from '@/database/skill';
import article from '@/database/article';
import code from '@/database/code';

export default {
  components: {
    personal: Personal,
    boxs: Boxs,
  },
  data() {
    return {
      user,
      code,
      skill,
      article,
      experience,
      codeTitle: 'Open Source',
      experienceTitle: 'Experiences',
      skillTitle: 'Skills',
      articleTitle: 'Article',
    };
  },
};
</script>
