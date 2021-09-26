<template>
  <div id="home" class="container">
    <Banner id="main-banner" :src="require('@/assets/banner.jpg')">
      <div id="info-text">
        <img src="@/assets/logo.png">
        <p>
          Welcome to my small corner of the internet; my name is Chris (aka <span class="highlight">Hazdryx</span>). I'm a C# and JavaScript software developer.
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
  #main-banner > img {
    filter: grayscale(0.66) brightness(0.5);
  }

  #info-text {
    position: absolute;
    width: 36em;
    max-width: 100%;
    padding: 1em;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  #info-text > img {
    position: relative;
    left: 50%;
    transform: translate(-50%, 0);
    height: 28em;
    margin-bottom: 1em;
  }
  #info-text > p {
    text-align: center;
  }
  #info-text span.highlight {
    background: linear-gradient(to right, #5AE, #A5E);
    background-clip: text;
    color: transparent;
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
