<template>
  <div class="nav">
    <div class="nav__item" @click="scrollToSection('home')">Home</div>
    <div class="nav__item" @click="scrollToSection('about')">About</div>
    <div class="nav__item" @click="scrollToSection('skills')">Skills</div>
    <div class="nav__item" @click="scrollToSection('career')">Career</div>
    <div class="nav__item" @click="scrollToSection('works')">Works</div>
    <div class="nav__item" @click="scrollToSection('contacts')">Contacts</div>
  </div>
</template>

<script>
export default {
  name: "Nav",
  methods: {
    clickArrow() {
      const number = Math.round(window.scrollY / window.innerHeight);
      const target = window.innerHeight * number;
      window.scroll({ top: target, behavior: "smooth" });
    },
    scrollToSection(id) {
      this.currentSection = id;
      const section = document.querySelector(`#${id}`);
      const offsetTop = section.getBoundingClientRect().top;
      const target = offsetTop + window.scrollY;
      window.scrollTo({ top: target, behavior: "smooth" });
    }
  }
};
</script>

<style lang="scss">
.nav {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  box-sizing: border-box;
  background: var(--backgrounColor);
  border-left: 1px solid var(--grayColor);
  padding: 100px 0;
  width: 100px;
  height: 100%;
  position: fixed;
  top: 0;
  right: 0;

  &__item {
    font-size: 14px;
    text-transform: uppercase;
    writing-mode: vertical-lr;
    color: var(--darkColor);
    transition: 0.33s ease;

    &:hover {
      cursor: pointer;
      color: var(--brandColor);
    }
  }
}
</style>