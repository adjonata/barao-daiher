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

<style lang="scss">
$shadow: rgba(0, 0, 0, 0.35) 0px 3px 8px;

.flavor-item {
  background: #fff;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin: 15px 35px 25px;
  border-radius: 9px;
  -webkit-box-shadow: $shadow;
  box-shadow: $shadow;

  @media (max-width: $mobile) {
    margin: 15px 10px 25px 10px;
  }

  &__image {
    order: 2;
    width: 170px;
    height: 281.33px;
    border-radius: 9px;
    filter: contrast(110%);
    border-bottom: solid 5px $dark-grey;

    @media (max-width: $mobile) {
      width: 140px;
      height: auto;
    }
  }

  &__title {
    order: 1;
    width: 100%;
    line-height: 40px;
    font-size: 15px;
    font-weight: normal;
    background: $dark-grey;
    color: #f1f1f1;
    border-radius: 10px 10px 0 0;
    margin: 0 0 -5px 0;
    -webkit-box-shadow: $shadow;
    box-shadow: $shadow;
    z-index: 10;
  }
}
</style>
