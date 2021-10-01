<template>
<div class="project">
  <div>
    <img :src="this.img" />
  </div>
  <div>
    <a class="title" :href="this.href" :style="{color: rgba(this.color)}"><h2>{{this.name}}</h2></a><br>
    <div class="content">
      <slot></slot>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Project',
  props: ['name', 'href', 'img'],
  methods: {
    rgba(col) {
      return `rgba(${col.r}, ${col.g}, ${col.b}, ${col.a})`
    },
    calcY() {
      this.y = (this.$el.offsetTop - window.scrollY) / (window.innerHeight / 1.5) - 0.25;
      this.y = this.y >= 0 ? this.y <= 1 ? this.y : 1 : 0;

      this.color.r = this.y * 16 + (1 - this.y) * 148;
      this.color.g = (1 - this.y) * 16 + (this.y) * 148;
      this.color.b = 216;
    }
  },
  data() {
    return {
      y: 0,
      color: { r: 0, g: 0, b: 0, a: 1 }
    }
  },
  mounted() {
    window.addEventListener('scroll', this.calcY);
    this.calcY();
  }
}
</script>

<style>
.project {
  width: 100%;
  display: flex;
  justify-content: center;
}
.project:nth-child(even) {
  flex-direction: row-reverse;
}
.project > div {
  width: 50vh;
  padding: 0 1em;
  margin: 1.5em 0;
}
.project > div:first-child {
  position: relative;
}
.project > div:first-child > img {
  position: relative;
  top: 50%; 
  transform: translate(0, -50%);
  width: 50%;
}

.project .title {
  text-decoration: none;
}
.project .title:hover {
  text-decoration: underline;
}

.project:nth-child(odd) > div:first-child, .project:nth-child(even) > div:last-child {
  border-right: 1px solid #CCC;
  text-align: right;
}
</style>