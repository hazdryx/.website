<template>
  <div class="banner">
    <img :src="this.src" />
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Banner',
  props: ['src']
}
</script>

<style>
  .banner {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
    color: #EEE;
  }
  .banner > img {
    position: absolute;
    object-fit: cover;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
  .banner > .content {
    position: relative;
    z-index: 1;
    width: 100%;
    height: 100%;
  }
</style>