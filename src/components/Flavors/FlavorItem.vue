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
  -webkit-box-shadow: -1px 5px 8px 4px rgba(0, 0, 0, 0.24);
  box-shadow: -1px 5px 8px 4px rgba(0, 0, 0, 0.24);
  border-radius: 10px;

  @media (max-width: $mobile) {
    margin: 15px 10px;
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
    background: $burned-yellow-2;
    color: #f1f1f1;
    border-radius: 0 0 10px 10px;
  }
}
</style>
