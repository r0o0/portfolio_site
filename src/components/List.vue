<template>
  <div class="list">
    <ul class="portfolio-list">
      <li v-for="item in listData" v-bind:key="item.title">
        <h3 class="title">
          {{ item.title }}
          <span class="year">{{ item.year }}</span>
          <span v-if="item.ongoing" class="ongoing">In progress</span>
        </h3>
        <p class="description">
          {{ item.description }}
        </p>
        <p class="role"><b class="subtitle">Role:</b><span>{{ item.role }}</span></p>
        <div class="links">
          <b class="subtitle">링크:</b>
          <ul>
            <li
              v-for="link in item.links"
              v-bind:key="link.name"
            >
             <a
              v-if="link.name === 'Portfolio'"
              v-bind:href="link.link"
              download
            >
              {{ link.name }}
            </a>
             <a v-else v-bind:href="link.link" target="_blank">{{ link.name }}</a>
            </li>
          </ul>
        </div>
        <div v-show="$route.path === '/developer'" class="tags">
          <span v-for="tag in item.tags" v-bind:key="tag">
            {{ tag }}
          </span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    listData: Array,
  },
};
</script>

<style scoped lang="scss">
.portfolio-list {
  & > *:not(:last-child) {
    width: 100%;
    height: inherit;
    margin-bottom: 16px;
    padding: 16px 0;
    border-bottom: 1px solid #313030;
  }
  & > li:last-child {
    padding: 16px 0;
    margin-bottom: 40px;
  }
  .title {
    margin-bottom: 12px;
    font-size: 28px;
    font-weight: bold;
    .year {
      margin-left: 4px;
      font-size: 14px;
      color: #898787;
    }
    .ongoing {
      margin-left: 16px;
      font-size: 14px;
      color: #42b983;
    }
  }
  .description {
    margin-bottom: 10px;
    color: #aeadad;
    line-height: 1.48em;
  }
  .role {
    display: inline-block;
    margin-bottom: 12px;
  }
  .links {
    display: flex;
    margin-bottom: 16px;
    ul {
      display: flex;
      & li > * {
        margin-right: 12px;
        color: #fff;
      }
    }
  }
  .tags {
    display: flex;
    align-items: center;
    margin-bottom: 24px;
    & > * {
      display: flex;
      align-items: center;
      margin-right: 8px;
      padding: 6px 14px;
      font-size: 14px;
      font-weight: bold;
      color: #c5c2c2;
      background: #302e2e;
      border-radius: 40px;
      vertical-align: center;
    }
  }
  .subtitle {
    margin-right: 6px;
    font-weight: bold;
    color: #949191;
  }
}
</style>
