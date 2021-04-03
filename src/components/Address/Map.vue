<template>
  <iframe
    :src="source"
    width="600"
    height="450"
    frameborder="0"
    style="border: 0"
    allowfullscreen=""
    aria-hidden="false"
    tabindex="0"
  />
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

<style lang="scss" scoped></style>
