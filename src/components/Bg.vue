<template>
  <div class="bg">
    <div class="bg__item">Javascript</div>
    <div class="bg__item">ES5</div>
    <div class="bg__item">ES6</div>
    <div class="bg__item">jQuery</div>
    <div class="bg__item">Vue</div>
    <div class="bg__item">Scss</div>
    <div class="bg__item">Less</div>
    <div class="bg__item">Git</div>
    <div class="bg__item">Workflow</div>
    <div class="bg__item">Webpack</div>
    <div class="bg__item">Gulp</div>
    <div class="bg__item">Babel</div>
    <div class="bg__item">ESLint</div>
    <div class="bg__item">Stylelint</div>
    <div class="bg__item">Pretter</div>
    <div class="bg__item">NodeJS</div>
    <div class="bg__item">Jess</div>
    <div class="bg__item">Moca</div>
  </div>
</template>

<script>
import Helper from "@/modules/helper";
export default {
  name: "Bg",
  data() {
    return {
      bgItems: null
    };
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      this.bgItems = document.querySelectorAll(".bg__item");
      this.animationBg();
    },
    animationBg() {
      this.bgItems.forEach(item => {
        const w = window.innerWidth - 100;
        const h = window.innerHeight - 100;
        const x = Helper.random(100, w);
        const y = Helper.random(100, h);
        item.style.top = `${y}px`;
        item.style.left = `${x}px`;
      });
    }
  }
};
</script>

<style lang="scss">
.bg {
  overflow: hidden;
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;

  &__item {
    opacity: 0.15;
    position: absolute;
    font-size: 14px;
    font-weight: bold;
    transition: 9s linear;
  }
}
</style>