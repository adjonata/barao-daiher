<template>
  <Container id="sabores" class="flavors" title="Sabores">
    <div class="flavors-list">
      <FlavorItem
        v-for="(flavor, index) in flavors"
        :key="'flavor_' + index"
        :image="flavor.image"
        :title="flavor.title"
      />
    </div>
  </Container>
</template>

<script>
import flavors from '@/utils/flavors'
import FlavorItem from './FlavorItem'

export default {
  name: 'Flavors',
  components: { FlavorItem },
  data: () => ({
    flavors,
  }),
}
</script>

<style lang="scss" scoped>
.flavors {
  margin-top: 50px;
  padding-left: 0;
  padding-right: 0;

  @media (max-width: $mobile) {
    margin-top: 20px;
  }

  &-list {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;

    @media (max-width: $mobile) {
      overflow-x: auto;
      flex-wrap: nowrap;
      justify-content: flex-start;

      .flavor-item {
        &:first-child {
          margin-left: 15px;
        }
        &:last-child {
          margin-right: 20px;
        }
      }
    }
  }
}
</style>
