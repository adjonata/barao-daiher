<template>
  <div class="socials">
    <h4 class="socials__title">Contatos:</h4>
    <a
      v-for="(social, i) in socials"
      :key="'social_' + i"
      :href="social.link || '#'"
      class="socials__link"
      :style="social.background ? { background: social.background } : {}"
    >
      {{ social.name }}
    </a>
  </div>
</template>

<script>
export default {
  name: 'Socials',
  data: () => ({
    socials: [
      {
        name: 'Whatsapp',
        link: 'https://api.whatsapp.com/send?phone=5515996712158',
        background: '#25D366',
      },
      {
        name: 'Facebook',
        link: 'https://www.facebook.com/profile.php?id=100002789737374',
        background: '#4267B2',
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.socials {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;

  color: #f1f1f1;

  &__title {
    display: none;
    text-align: left;
    font-size: 20px;
    font-weight: 400;
  }

  &__link {
    text-decoration: none;
    color: #f1f1f1;
    font-size: 16px;
    width: 200px;
    line-height: 50px;

    @media (max-width: $mobile) {
      line-height: 40px;
    }

    margin: 8px;
    border-radius: 8px;
  }
}
</style>
