<template>
  <Container title="Onde nos encontrar" id="onde-nos-encontrar" class="address">
    <Map />
  </Container>
</template>

<script>
import Map from './Map'

export default {
  name: 'Address',
  components: { Map },
}
</script>

<style lang="scss" scoped></style>
