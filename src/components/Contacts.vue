<template>
  <div id="contacts" class="contacts section">
    <div class="container">
      <div class="section__wrapper">
        <div class="section__left">
          <div class="section__title">Contacts</div>
        </div>
        <div class="section__right">
          <div class="contacts__item">Phone | +7 951 480 3426</div>
          <div class="contacts__item">E-mail | dementevms@gmail.com</div>
          <div class="contacts__item">Skype | Dementevms</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contacts"
};
</script>

<style lang="scss">
.contacts {
  &__item {
    margin: 40px 0;
    font-size: 24px;
    font-weight: bold;
    color: var(--darkColor);
  }
}
</style>