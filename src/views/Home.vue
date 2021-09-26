<template>
  <div id="home" class="container">
    <Banner :src="require('@/assets/banner.jpg')">
      <div id="info-text">
        <h1 style="font-size: 8em; text-align: center; margin-bottom: 0.8rem">Hazdryx</h1>
        <p>
          Welcome to my small corner of the internet; my name is Chris (aka Hazdryx). I'm a C# and JavaScript software developer.
          This website is still in the works, but feel free to check out my socials and GitHub!
        </p>
      </div>
      <div id="info-socials">
        <a href="https://github.com/hazdryx" class="icon"><fa-icon :icon="['fab', 'github']" /></a>
        <a href="https://linkedin.com/in/hazdryx" class="icon"><fa-icon :icon="['fab', 'linkedin']" /></a>
        <a href="https://twitter.com/hazdryx" class="icon"><fa-icon :icon="['fab', 'twitter']" /></a>
        <a href="https://facebook.com/hazdryx" class="icon"><fa-icon :icon="['fab', 'facebook']" /></a>
        <a href="https://github.com/hazdryx/.website" class="icon"><fa-icon :icon="['fas', 'code-branch']" /></a>
      </div>
    </Banner>
  </div>
</template>

<script>
// @ is an alias to /src
import Banner from '@/components/Banner.vue';

export default {
  name: 'Home',
  components: {
    Banner
  }
}
</script>

<style>
  #info-text {
    position: absolute;
    width: 38em;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  #info-socials {
    position: absolute;
    bottom: 1em;
    width: 100%;
    text-align: center;
  }

  a.icon {
    margin: 0.25em;
    color: #EEE;
  }
  a.icon:hover {
    color: #CCC;
  }
  a.icon > svg {
    font-size: 2.5em;
  }
</style>
