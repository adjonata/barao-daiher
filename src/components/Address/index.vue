<template>
  <Container title="Onde encontrar" id="onde-encontrar" background="#fafafa">
    <div class="address">
      <Infos />
      <Map />
    </div>
  </Container>
</template>

<script>
import Map from './Map'
import Infos from './Infos'

export default {
  name: 'Address',
  components: { Map, Infos },
}
</script>

<style lang="scss">
.address {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 60px;
  padding-top: 40px;

  // In Mobile
  @media (max-width: $mobile) {
    .address-infos {
      order: 2;
    }

    padding: 10px 30px;
    flex-direction: column;
  }
}
</style>
