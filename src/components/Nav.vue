<template>
  <nav class="nav">
    <router-link to="/developer">개발</router-link>
    <router-link to="/designer">디자인</router-link>
  </nav>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
.nav {
  & > * {
    color: inherit;
  }
  & > *:not(:last-child) {
    margin-right: 12px;
  }
}
</style>
