<template>
  <div :class="{socials: true, scroll: isFixed}">
    <a v-for="social in socials" :key="social.href" :href="social.href"><fa-icon :icon="social.icon" /></a>
  </div>
</template>

<script>
export default {
  name: 'Socials',
  props: ['socials', 'fixed'],
  data() {
    return { 
      isFixed: this.fixed
    };
  },
  mounted() {
    window.addEventListener('scroll', e => {
      this.isFixed = this.fixed || window.scrollY > window.innerHeight - this.$el.clientHeight;
    });
  }
}
</script>

<style>
  .socials {
    position: absolute;
    z-index: 2;
    bottom: 0;
    padding: 0.75em;
    width: 100%;
    height: max-content;
    text-align: center;
  }
  .socials.scroll {
    position: fixed;
    top: 0;
    background-color: rgba(0, 0, 0, 0.9);
  }

  .socials > a {
    margin: 0.25em;
    color: #EEE;
  }
  .socials > a:hover {
    color: #CCC;
  }
  .socials > a > svg {
    font-size: 2.5em;
  }
</style>