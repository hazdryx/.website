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
  }
  .banner > img {
    position: absolute;
    object-fit: cover;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
  }
  .banner > .content {
    position: absolute;
    z-index: 1;

    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
</style>