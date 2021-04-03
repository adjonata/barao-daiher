<template>
  <section class="container">
    <div class="container-content">
      <h3 class="container-title" v-if="title">{{ title }}</h3>
      <slot />
    </div>
  </section>
</template>

<script>
export default {
  name: 'Container',
  props: {
    title: String,
  },
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  padding: 40px 20px;
  display: flex;
  justify-content: center;

  @media (max-width: $mobile) {
    padding: 15px;
  }

  &-content {
    width: 100%;
    max-width: 1344px;
    text-align: center;
  }

  &-title {
    width: 100%;
    font-size: 21px;
    color: $dark;
    margin-bottom: 40px;
    text-transform: uppercase;

    @media (max-width: $mobile) {
      font-size: 17px;
      margin-bottom: 20px;
    }

    &::before {
      content: '----';
      letter-spacing: -2px;
      margin-right: 12px;
      color: $grey;
    }
    &::after {
      content: '----';
      letter-spacing: -2px;
      margin-left: 12px;
      color: $grey;
    }
  }
}
</style>
