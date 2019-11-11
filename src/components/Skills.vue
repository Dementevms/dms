<template>
  <div id="skills" class="skills section">
    <div class="container">
      <div class="skills__wrapper container__wrapper">
        <div class="skills__item">Skills:</div>
        <div class="skills__item">Javascript</div>
        <div class="skills__item">ES5</div>
        <div class="skills__item">ES6</div>
        <div class="skills__item">VueJS</div>
        <div class="skills__item">NuxtJS</div>
        <div class="skills__item">jQuery</div>
        <div class="skills__item">HTML 5</div>
        <div class="skills__item">CSS</div>
        <div class="skills__item">SVG</div>
        <div class="skills__item">Scss</div>
        <div class="skills__item">Less</div>
        <div class="skills__item">Webpack</div>
        <div class="skills__item">Gulp</div>
        <div class="skills__item">Babel</div>
        <div class="skills__item">ESLint</div>
        <div class="skills__item">Stylelint</div>
        <div class="skills__item">Pretter</div>
        <div class="skills__item">Jest</div>
        <div class="skills__item">Mocha</div>
        <div class="skills__item">Cypress</div>
        <div class="skills__item">NodeJS</div>
        <div class="skills__item">Express</div>
        <div class="skills__item">MongoDB</div>
        <div class="skills__item">Puppeteer</div>
        <div class="skills__item">Git</div>
        <div class="skills__item">Workflow</div>
        <div class="skills__item">...</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Skills"
};
</script>

<style lang="scss">
.skills {
  &__wrapper {
    display: flex;
    flex-wrap: wrap;
  }

  &__item {
    background: var(--darkColor);
    margin: 10px;
    padding: 10px;
    font-size: 24px;
    font-weight: bold;
    color: var(--whiteColor);

    &:first-child {
      background: var(--brandColor);
    }
  }
}
</style>