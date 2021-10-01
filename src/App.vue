<template>
  <Socials :socials="[
    { href: 'https://github.com/hazdryx', icon: ['fab', 'github'] },
    { href: 'https://linkedin.com/in/hazdryx', icon: ['fab', 'linkedin'] },
    { href: 'https://twitter.com/hazdryx', icon: ['fab', 'twitter'] },
    { href: 'https://facebook.com/hazdryx', icon: ['fab', 'facebook'] },
    { href: 'https://github.com/hazdryx/.website', icon: ['fas', 'code-branch'] }
  ]" />
  <router-view />
</template>

<script>
import Socials from '@/components/Socials';

export default {
  components: {
    Socials
  }
};
</script>

<style>
  body {
    color: #111;
    background-color: #EEE;
  }
</style>
