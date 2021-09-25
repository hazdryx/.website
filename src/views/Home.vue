<template>
  <div id="home" class="container">
    <Banner :src="require('@/assets/banner.jpg')">
      <div style="width: 38em">
        <h1 style="font-size: 8em; text-align: center; margin-bottom: 0.8rem">Hazdryx</h1>
        <p>
          Welcome to my small corner of the internet, my name is a Chris (aka Hazdryx). I'm a C# and JavaScript software developer.
          This website is still in the works, but feel free to check out my socials and GitHub!
        </p>
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
