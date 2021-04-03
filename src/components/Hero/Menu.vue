<template>
  <div class="menu">
    <a
      v-for="(item, index) in sections"
      :key="'item_' + index"
      :href="item.to || ''"
    >
      {{ item.title }}
    </a>
  </div>
</template>

<script>
import sections from '@/utils/sections'

export default {
  name: 'Menu',
  data: () => ({
    sections,
  }),
}
</script>

<style lang="scss" scoped>
.menu {
  display: flex;
  align-items: center;

  a {
    text-decoration: none;
    color: #f1f1f1;
    text-transform: uppercase;
    font-size: 14px;
    transition: color 0.3s;
    font-weight: 600;
    padding: 8px 15px;
    border-radius: 8px;
    text-align: center;
    // border: solid 1px #3d3d3d;

    &:not(:last-child) {
      margin-right: 15px;
    }

    &:hover {
      color: #e0e0e0;
    }
  }
}
</style>
