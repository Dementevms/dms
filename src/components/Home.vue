<template>
  <div id="home" class="home section">
      <div class="container">
        <div class="container__wrapper">
          <div class="home__title">Dementyev Mikhail</div>
          <div class="home__subtitle">Frontend developer</div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style lang="scss">
.home {
  &__title {
    margin: 0 0 40px;
    font-size: 76px;
    font-weight: bold;
    color: var(--darkColor);
  }

  &__subtitle {
    font-size: 36px;
    color: var(--darkColor);
  }
}
</style>