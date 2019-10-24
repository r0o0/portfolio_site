<template>
  <div id="app">
    <header class="header">
      <h1 class="logo">
        <router-link to="/">오나경</router-link>
      </h1>
      <Nav v-show="$route.path !== '/'" />
    </header>
    <main>
      <router-view/>
    </main>
    <footer class="footer">
      Na Kyung Oh | r0o0 © 2019
    </footer>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue';

export default {
  components: {
    Nav,
  },
};
</script>

<style lang="scss">
#app {
  display: flex;
  flex-flow: column wrap;
  justify-content: space-between;
  width: 100%;
  height: 100%;
  overflow-x: hidden;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #e2dede;
  background: #161616;
  cursor: default;
}
.header {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  align-content: center;
  width: 100%;
  height: 72px;
  padding: 0 16px;

  @media screen and (min-width: 764px) {
    padding: 0 40px;
  }
  @media screen and (min-width: 1440px) {
    padding: 0 80px;
  }
  .logo {
    font-size: 20px;
    font-weight: bold;
    cursor: pointer;
    & > * {
      text-decoration: none;
      color: inherit;
    }
  }
}
.footer {
  height: 40px;
  margin-top: 32px;
  padding: 0 16px;
  font-size: 14px;
  color: #b0adad;
  @media screen and (min-width: 764px) {
    padding: 0 40px;
  }
  @media screen and (min-width: 1440px) {
    padding: 0 80px;
  }
}
</style>
