<template>
  <header class="hero">
    <div class="hero__wrapper">
      <div class="hero__wrapper-head">
        <Logo />
        <Menu />
      </div>
      <div class="hero__wrapper-details">
        <p>
          " A ressaca é o preço que se paga por algo que nem lembro direito, mas
          sei que foi divertido "
        </p>
        <ProductCard />
      </div>
    </div>
  </header>
</template>

<script>
import ProductCard from './ProductCard'
import Logo from './Logo'
import Menu from './Menu'

export default {
  name: 'Hero',
  components: { ProductCard, Logo, Menu },
}
</script>

<style lang="scss" scoped>
.hero {
  width: 100%;
  background: linear-gradient(
    -30deg,
    $dark 34.67%,
    $dark 34.67%,
    $burned-yellow 167.29%
  );
  display: flex;
  justify-content: center;

  &__wrapper {
    max-width: 1344px;
    width: 100%;

    &-head {
      width: 100%;
      padding: 25px 30px 15px;
      display: flex;
      align-items: center;
      justify-content: space-between;

      @media (max-width: $mobile) {
        flex-direction: column;
        align-items: flex;
        justify-content: flex-start;

        .logo {
          margin-bottom: 35px;
        }
      }
    }

    &-details {
      height: 300px;
      padding: 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;

      p {
        color: #e6e6e6;
        font-size: 24px;
        max-width: 530px;
        padding-bottom: 40px;
        letter-spacing: 1px;
        font-family: 'New Tegomin', sans-serif;
      }

      .product-card {
        align-self: flex-end;
        margin-bottom: -120px;
      }

      @media (max-width: $mobile) {
        height: auto;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        padding: 15px 30px;
        text-align: center;

        p {
          font-size: 18px;
          color: #c5c5c5;
        }
      }
    }
  }
}
</style>
