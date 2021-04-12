<template>
  <div class="links">
    <div
      class="links-item"
      v-for="(link, index) in links"
      :key="'link_' + index"
    >
      <span> {{ link.label }}</span>
      <a :href="link.url" target="_blank">{{ link.text }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Links',
  data: () => ({
    links: [
      {
        label: 'E-Mail para contato:',
        text: 'barao.daiher@gmail.com',
        url: 'mailto:barao.daiher@gmail.com',
      },
      {
        label: 'Desenvolvedor:',
        text: 'welcometoalex.space',
        url: 'https://welcometoalex.space',
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.links {
  &-item {
    text-align: center;
    display: flex;
    flex-direction: column;

    &:not(:first-child) {
      margin-top: 25px;
    }

    span {
      margin-bottom: 4px;
    }

    a {
      text-decoration: none;
      color: $grey;
    }
  }
}
</style>
