<template>
  <div id="home" class="container">
    <Banner id="main-banner" :src="require('@/assets/banner.jpg')">
      <div id="info-text">
        <img src="@/assets/logo.png">
        <p>
          Welcome to my small corner of the internet; my name is Chris 
          (aka <span class="highlight">Hazdryx</span>). I'm a C# and 
          JavaScript developer passionate about creating great software and 
          libraries to support them.
        </p>
      </div>
    </Banner>

    <!-- Projects -->
    <div>
      <h1 class="header">Open Source</h1>
      <Project name="FastBitmap" href="https://github.com/hazdryx/FastBitmap" :img="require('@/assets/projects/fastbitmap.svg')">
        <p>
          FastBitmap is a .NET library that wraps the System.Drawing.Bitmap class 
          for improved pixel read/write performance. I wrote this library to provide 
          an intuitive platform for image manipulation on .NET Standard, similar 
          to GetPixel and SetPixel on the original Bitmap. It now provides more 
          functionality to make it faster, such as bulk pixel operations and manipulating 
          the image using primitives.
        </p>
      </Project>
      <Project name="cino" href="https://github.com/hazdryx/cino" :img="require('@/assets/projects/cino.svg')">
        <p>
          Clock In N' Out (aka cino) is a cli timesheet application differentiated by workspaces, built using the Node.js platform.
        </p>
      </Project>
      <Project name="lendr" href="https://github.com/hazdryx/lendr-frontend" :img="require('@/assets/projects/lendr.svg')">
        <p>
          lendr is a minimalistic web app built on the MEVN stack for tracking loans 
          between friends and family. I created this because I was lending money to 
          my friends and family frequently. It features a userless system, which uses 
          lender and borrower tokens instead to manage the data. I also implemented a 
          simplistic autopay system so I wouldn't forget to update it.
        </p>
      </Project>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Banner from '@/components/Banner.vue';
import Project from '@/components/Project.vue';

export default {
  name: 'Home',
  components: {
    Banner, Project
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

  h1.header {
    font-size: 4em;
    text-align: center;
    color: #222;
    letter-spacing: 0.1em;
    padding: 1rem 0 0.5rem 0;
  }
</style>
