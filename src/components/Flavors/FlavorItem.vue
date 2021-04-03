<template>
  <article class="flavor-item">
    <img :src="image" alt="Imagem do produto.jpeg" class="flavor-item__image" />
    <h3 class="flavor-item__title">{{ title }}</h3>
  </article>
</template>

<script>
export default {
  name: 'FlavorItem',
  props: {
    /**
     * Imagem do produto
     */
    image: {
      type: String,
      required: true,
    },
    /**
     * Título do produto
     */
    title: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.flavor-item {
  background: #fff;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin: 15px 35px 25px;
  -webkit-box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px, -4px 4px 0 0px $dark-grey;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px, -4px 4px 0 0px $dark-grey;
  border-radius: 10px;

  @media (max-width: $mobile) {
    margin: 15px 10px 25px 10px;
  }

  &__image {
    width: 170px;
    height: 281.33px;
    border-radius: 10px 10px 0 0;
    filter: contrast(110%);

    @media (max-width: $mobile) {
      width: 140px;
      height: auto;
    }
  }

  &__title {
    width: 100%;
    line-height: 40px;
    font-weight: lighter;
    font-size: 15px;
    font-weight: 600;
    background: linear-gradient(to bottom, $burned-yellow, $burned-yellow-2);
    color: #f1f1f1;
    border-radius: 0 0 10px 10px;
    margin-top: -15px;
    z-index: 10;
  }
}
</style>
