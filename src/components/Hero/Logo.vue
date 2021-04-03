<template>
  <div :class="['logo', { small: isSmallViewport }]">
    <img :src="Logo" alt="Logo.png" />
    <div class="logo-text">
      <h3>Barão Daiher</h3>
      <h4>Cachaças artesanais</h4>
    </div>
  </div>
</template>

<script>
import Logo from '@/assets/logo.png'

export default {
  name: 'Logo',
  data: () => ({
    Logo,
  }),
  computed: {
    isSmallViewport() {
      return window.innerWidth <= 768
    },
  },
}
</script>

<style lang="scss" scoped>
.logo {
  display: flex;
  align-items: center;

  img {
    width: 45px;
  }

  &-text {
    display: flex;
    flex-direction: column;
    margin-left: 9px;

    h3 {
      color: #fff;
      font-size: 20px;
      font-weight: 600;
      letter-spacing: -0.2px;
      text-transform: capitalize;
    }

    h4 {
      font-size: 13px;
      color: #d1d1d1;
      font-weight: 500;
    }
  }

  &.small {
    h3 {
      text-transform: uppercase !important;
    }
  }
}
</style>
