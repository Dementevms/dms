<template>
  <div id="about" class="about section">
    <div class="container">
      <div class="section__wrapper">
        <div class="section__left">
          <div class="section__title">About</div>
        </div>
        <div class="section__right">
          <div class="about__image">
            <img src="@/assets/images/about.png" alt="about" />
          </div>
          <div
            class="about__text"
          >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris vel mattis lorem, at pellentesque erat. Fusce hendrerit, turpis ac suscipit sagittis, erat mauris hendrerit mauris, eu laoreet ipsum quam id mi. Donec condimentum nunc leo, quis volutpat ipsum finibus quis. Duis volutpat rhoncus augue, id semper ligula tempus sed. Praesent nisl massa, varius id imperdiet non, finibus et tellus. Aliquam suscipit maximus tortor nec ornare. Donec efficitur facilisis metus vitae sollicitudin. Donec scelerisque, magna non facilisis euismod, ex leo sollicitudin quam, sed pulvinar dolor est nec justo. Etiam vel lacinia ex. Vestibulum nec consectetur elit. Phasellus bibendum ipsum eget gravida mollis. Cras venenatis gravida urna, et mattis risus mattis sit amet. Phasellus quis nulla ut metus tincidunt rutrum in sit amet ante. Nulla sed elit a tortor ornare pellentesque. Mauris tincidunt, lorem ut dictum porta, dolor lectus porta arcu, a facilisis turpis dolor ac quam.</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About"
};
</script>

<style lang="scss">
.about {
  &__image {
    overflow: hidden;
    background: var(--darkColor);
    margin: 0 0 40px;
    width: 300px;
    height: 300px;
    position: relative;

    img {
      width: 100%;
    }

    &::after {
      display: block;
      content: "";
      background: var(--darkColor);
      opacity: 0.3;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }
  }

  &__text {
    font-size: 18px;
    line-height: 30px;
    color: var(--darkColor);
  }
}
</style>