<template>
  <div class="developer">
    <h2 class="headline">프론트엔드 개발자로 전향하면서 작업한 개인 프로젝트들입니다.</h2>
    <List v-bind:list-data="list"/>
  </div>
</template>

<script>
import List from '@/components/List.vue';

export default {
  data() {
    return {
      list: [
        {
          title: 'Brote',
          year: '2019',
          description: '최근에 React로 작업한 Medium 서비스와 같은 퍼블리싱 앱입니다.',
          role: 'Frontend, Backend',
          tags: [
            'React', 'Typescript', 'Redux', 'Slate', 'Material-UI', 'Emotion', 'Apollo-client', 'Now', 'Prisma', 'Graphql api',
          ],
          links: [
            {
              name: 'Github',
              link: 'https://github.com/r0o0/brote-app',
            },
            {
              name: 'Demo',
              link: 'https://brote.r0o0.now.sh',
            },
          ],
          ongoing: true,
        },
        {
          title: 'Detoxer',
          year: '2019',
          description: '현재 진행중인 Vue로 작업중인 쇼핑몰입니다.',
          role: 'Frontend',
          tags: [
            'Vue', 'Pug', 'Scss', 'Firebaseui', 'Firebase Auth',
          ],
          links: [
            {
              name: 'Github',
              link: 'https://github.com/r0o0/detoxer',
            },
          ],
          ongoing: true,
        },
        {
          title: 'Todo',
          year: '2019',
          description: 'Firebase로 Rest api를 이용하고 React로 작업한 Todo입니다.',
          role: 'Frontend',
          tags: [
            'React', 'Firebase', 'Rest api', 'Sass',
          ],
          links: [
            {
              name: 'Github',
              link: 'https://github.com/r0o0/simpleTodo-react',
            },
            {
              name: 'Demo',
              link: 'https://todo-react-7293.firebaseapp.com/',
            },
          ],
          ongoing: false,
        },
        {
          title: 'Movie Search',
          year: '2018',
          description: 'Tmdb api를 사용하여 영화를 검색 할 수 있는 toy project입니다.',
          role: 'Frontend',
          tags: [
            'React', 'Tmdb api', 'Redux', 'Sass',
          ],
          links: [
            {
              name: 'Github',
              link: 'https://github.com/r0o0/movie-search-react',
            },
            {
              name: 'Demo',
              link: 'https://r0o0.github.io/movie-search-react/',
            },
          ],
          ongoing: false,
        },
        {
          title: 'Carousels',
          year: '2019 & 2018',
          description: 'Carousel 모음집입니다. 하나는 Vanilla JS로 작업하였고 나머지는 최근에 Vue 프레임워크를 사용하여 작업했습니다.',
          role: 'Frontend',
          tags: [
            'Vue', 'Vanilla JS',
          ],
          links: [
            {
              name: 'Github',
              link: 'https://github.com/r0o0/carousels',
            },
          ],
          ongoing: false,
        },
      ],
    };
  },
  components: {
    List,
  },
};
</script>

<style lang="scss" scoped>
.developer {
  padding: 0 16px;
  @media screen and (min-width: 764px) {
    margin-left: 100px;
    padding: 0 40px;
  }
  @media screen and (min-width: 1440px) {
    margin-left: 200px;
    padding: 0 80px;
  }
  min-height: calc(100vh - 72px - 40px);
  .headline {
    margin: 32px 0;
    font-size: 24px;
    line-height: 1.3em;
    color: #a4a3a3;
    @media screen and (min-width: 764px) {
      font-size: 36px;
    }
  }
}
</style>
