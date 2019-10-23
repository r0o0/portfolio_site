<template>
  <div class="developer">
    <h2 class="headline">UI/UX 디자이너로서 작업한 개인 프로젝트들입니다.</h2>
    <div class="subcontent">
      <h3 class="subhead">Work</h3>
      <List v-bind:list-data="listWork"/>
    </div>
    <div class="subcontent">
      <h3 class="subhead">Personal</h3>
      <List v-bind:list-data="listPersonal"/>
    </div>
  </div>
</template>

<script>
import List from '@/components/List.vue';

export default {
  data() {
    return {
      listWork: [
        {
          title: 'Funded',
          year: '2016 - 2018',
          description: '대출자와 투자자를 이어주는 P2P 사이트 펀디드에서 사아트 유지보수 및 리뉴얼을 담당했습니다.',
          role: 'UX/UI, Planner, Publisher',
          tags: [],
          links: [
            {
              name: 'Portfolio',
              link: '../assets/2018_펀디드_오나경.pdf',
            },
            {
              name: 'Site',
              link: 'https://funded.co.kr',
            },
          ],
          ongoing: false,
        },
        {
          title: 'Marpple',
          year: '2016',
          description: '의류 커스터마이즈 서비스를 제공하는 쇼핑몰입니다. 마플의 사이트 리뉴얼을 담당했습니다.',
          role: 'UX/UI',
          tags: [],
          links: [
            {
              name: 'Case Study',
              link: 'http://xayx7293.cafe24.com/rayes/marpple.html',
            },
          ],
          ongoing: false,
        },
      ],
      listPersonal: [
        {
          title: 'Witmusic',
          description: '',
          role: 'App, Web, Responsive, UI/UX, Interaction Design',
          tags: [],
          links: [
            {
              name: 'Case Study',
              link: 'http://xayx7293.cafe24.com/rayes/music.html',
            },
          ],
          ongoing: false,
        },
        {
          title: 'Stark Bike',
          description: '',
          role: 'App, Web, UI/UX, Interaction Design',
          tags: [],
          links: [
            {
              name: 'Case Study',
              link: 'http://xayx7293.cafe24.com/rayes/bike.html',
            },
          ],
          ongoing: false,
        },
        {
          title: 'IBK 기업은행',
          description: '',
          role: 'Web, UI/UX',
          tags: [],
          links: [
            {
              name: 'Case Study',
              link: 'http://xayx7293.cafe24.com/rayes/bank.html',
            },
          ],
          ongoing: false,
        },
        {
          title: 'Lamborghini',
          description: '',
          role: 'Web, Interaction Design',
          tags: [],
          links: [
            {
              name: 'Case Study',
              link: 'http://xayx7293.cafe24.com/rayes/lamborghini.html',
            },
          ],
          ongoing: false,
        },
        {
          title: 'Avant Garders Thesis',
          description: '',
          role: 'App, Web, UI/UX, Interaction Design, Thesis',
          tags: [],
          links: [
            {
              name: 'Case Study',
              link: 'http://xayx7293.cafe24.com/rayes/avant.html',
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
  .subcontent {
    margin-bottom: 56px;
  }
  .subhead {
    position: relative;
    width: fit-content;
    margin-bottom: 10px;
    font-size: 18px;
    font-weight: bold;
    color: #a0a7a4;
    &::before {
      content: '👉';
      margin-right: 10px;
    }
  }
}
</style>
