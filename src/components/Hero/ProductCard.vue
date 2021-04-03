<template>
  <div class="product-card">
    <div class="product-card__images">
      <img :src="Copo" alt="Copo de vidro.png" class="copo" />
      <img :src="Cachaca" alt="Cachaca.png" class="cachaca" />
    </div>
  </div>
</template>

<script>
import Cachaca from '@/assets/cachaca_sem_fundo.png'
import Copo from '@/assets/copo_de_vidro.png'

export default {
  data: () => ({
    Cachaca,
    Copo,
  }),
}
</script>

<style lang="scss" scoped>
.product-card {
  padding: 20px;
  width: 290px;

  @media (max-width: $mobile) {
    display: none;
  }

  border-radius: 15px;
  background: #0c0702;
  box-shadow: 0 0 0 4px #fff;

  display: flex;
  justify-content: center;
  align-items: center;

  &__images {
    display: flex;
    align-items: center;
    height: 250px;

    @media (max-width: $mobile) {
      height: 200px;
    }

    .copo {
      display: none;
      opacity: 0.7;
      height: 70px;
      margin-bottom: 30px;
      filter: brightness(110%);
    }
    .cachaca {
      opacity: 0.8;
      height: 230px;

      @media (max-width: $mobile) {
        height: 180px;
      }
    }
  }
}
</style>
