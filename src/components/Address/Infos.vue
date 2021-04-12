<template>
  <article class="address-infos">
    <h4 class="address-infos__title">Endereço:</h4>

    <ul class="address-infos__list">
      <li v-for="(address, i) in addresses" :key="'address_' + i">
        <span class="material-icons">place</span>
        <h4>{{ makeAddress(address) }}</h4>
      </li>
    </ul>

    <h4 class="address-infos__title">Telefones:</h4>

    <ul class="address-infos__list">
      <li v-for="(telephone, i) in telephones" :key="'address_' + i">
        <span class="material-icons">phone</span>
        <a :href="'tel:' + telephone">{{ telephone }}</a>
      </li>
    </ul>
  </article>
</template>

<script>
export default {
  name: 'Infos',
  data: () => ({
    addresses: [{ city: 'Sorocaba', state: 'SP', street: null }],
    telephones: ['(15) 99671-2158', '(15) 99673-7593'],
  }),
  methods: {
    makeAddress(addressObject) {
      const order = ['street', 'city', 'state']

      let address = ''

      order.forEach((item, index) => {
        if (item in addressObject && addressObject[item]) {
          address += addressObject[item]
          if (index < order.length - 1) address += ', '
        }
      })

      return address
    },
  },
}
</script>

<style lang="scss" scoped>
.address-infos {
  text-align: left;
  display: flex;
  flex-direction: column;

  // In Mobile
  @media (max-width: $mobile) {
    width: 100%;
    margin-top: 30px;
  }

  // In Tablet and Desktop
  @media (min-width: $mobile) {
    min-width: 400px;
    padding: 30px 70px;
  }

  color: $dark;

  &__title {
    color: $dark;
    font-size: 25px;

    // In Mobile
    @media (max-width: $mobile) {
      font-size: 20px;
    }

    margin: 0 5px 10px;

    &:not(:first-child) {
      margin-top: 25px;
    }
  }

  &__list {
    list-style: none;

    li {
      width: 100%;
      display: flex;
      margin-bottom: 4px;
      font-size: 20px;

      @media (max-width: $mobile) {
        font-size: 16px;
      }

      span {
        margin-right: 6px;
        color: $yellow;
      }
      h4,
      a {
        color: $dark;
        text-decoration: none;
        font-weight: lighter;
      }
    }
  }
}
</style>
