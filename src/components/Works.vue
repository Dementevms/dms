<template>
  <div id="works" class="works section">
    <div class="container">
      <div class="works__wrapper container__wrapper">
        <div class="works__item" v-for="(item, index) in items" :key="index">
          <div class="works__item-image js-modal-open" data-type="image" :data-src="item.image">
            <img :src="item.imagePrev" alt />
          </div>
          <div class="works__item-title">{{ item.title }}</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Modal from "@/modules/modal";
export default {
  name: "Works",
  data() {
    return {
      items: [
        {
          title: "Artel",
          image: "images/artel.png",
          imagePrev: "images/artel_prev.png"
        },
        {
          title: "Unacare",
          image: "images/unacare.png",
          imagePrev: "images/unacare_prev.png"
        },
        {
          title: "Veziauto",
          image: "images/veziauto.png",
          imagePrev: "images/veziauto_prev.png"
        },
        {
          title: "L.E.P",
          image: "images/lep.png",
          imagePrev: "images/lep_prev.png"
        },
        {
          title: "Diplomnajarabota",
          image: "images/diplomnajarabota.png",
          imagePrev: "images/diplomnajarabota_prev.png"
        },
        {
          title: "Rusalochka",
          image: "images/rusalochka.png",
          imagePrev: "images/rusalochka_prev.png"
        }
      ]
    };
  },
  mounted() {
    new Modal();
  }
};
</script>

<style lang="scss">
.works {
  &__wrapper {
    display: flex;
    flex-wrap: wrap;
    margin: -30px;
    width: 100%;
  }

  &__item {
    background: #2c3e50;
    margin: 15px;
    width: calc(100% / 3 - 30px);
    position: relative;
  }

  &__item-title {
    position: absolute;
    bottom: 30px;
    left: 30px;
    font-size: 14px;
    font-weight: bold;
    color: var(--whiteColor);
  }

  &__item-image {
    overflow: hidden;
    position: relative;

    img {
      display: block;
      width: 100%;
      filter: grayscale(1);
      transition: 0.33s ease;
    }

    &::after {
      display: block;
      content: "";
      opacity: 1;
      background: var(--darkColor);
      opacity: 0.3;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    &:hover {
      cursor: pointer;

      img {
        filter: grayscale(0);
      }

      &::after {
        opacity: 0;
      }
    }
  }
}
</style>