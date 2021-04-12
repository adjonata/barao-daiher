<template>
  <Container background="#242424" id="contato">
    <footer>
      <div class="copyright">© Barão Daiher</div>
      <Links />
      <Socials />
    </footer>
  </Container>
</template>

<script>
import Socials from './Socials'
import Links from './Links'

export default {
  name: 'Footer',
  components: { Socials, Links },
}
</script>

<style lang="scss">
footer {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 50px;

  @media (max-width: $mobile) {
    flex-direction: column;
    padding: 15px 0;

    & > div {
      margin-bottom: 25px;
    }
  }
}
</style>
