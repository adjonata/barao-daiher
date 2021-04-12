<template>
  <div class="map">
    <iframe
      :src="source"
      frameborder="0"
      style="border: 0"
      allowfullscreen=""
      aria-hidden="false"
      tabindex="0"
    />
  </div>
</template>

<script>
import { source } from '@/utils/address'

export default {
  name: 'Map',
  data: () => ({
    source,
  }),
}
</script>

<style lang="scss">
.map {
  border: solid 5px $dark-grey;
  box-shadow: -5px 5px 0 0 $yellow;

  // In Mobile
  @media (max-width: $mobile) {
    width: 100%;
  }

  iframe {
    width: 800px;
    height: 400px;

    // In Mobile
    @media (max-width: $mobile) {
      width: 100%;
      height: 230px;
    }
  }
}
</style>
