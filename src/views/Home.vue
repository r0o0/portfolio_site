<template>
  <div class="home">
    <p class="headline">
      안녕하세요, 개발이 재미있어
      <br>
      개발자로 전향한 디자이너 출신
      <br>
      프론트엔드 개발자 오나경입니다.
    </p>
    <div class="portfolio-link">
      <strong class="caption">포트폴리오를 확인해보세요.</strong>
      <div class="links">
        <router-link to="/developer">개발</router-link>
        <router-link to="/designer">디자인</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  margin-top: -40px;
  padding: 0 24px;
  @media screen and (min-width: 764px) {
    margin-top: -210px;
    margin-left: 100px;
    padding: 0 40px;
  }
  @media screen and (min-width: 1440px) {
    margin-left: 200px;
    padding: 0 80px;
  }
  .headline {
    font-size: 30px;
    line-height: 1.45em;
  }
  .portfolio-link {
    display: flex;
    flex-flow: column wrap;
    margin-top: 32px;
    flex: 0 0 inherit;
    .caption {
      margin-bottom: 16px;
      font-size: 16px;
      font-weight: bold;
      color: #9a9a9a;
    }
    .links {
      display: flex;
      & > * {
        margin-right: 16px;
        padding: 12px 20px;
        text-decoration: none;
        font-size: 18px;
        font-weight: bold;
        color: #e2dede;
        border: 1px solid #ccc !important;
        border-radius: 4px;
        &:hover {
          background: rgba(255,255,255,0.3);
          transition: background 0.34s cubic-bezier(0.24, 0.52, 1, 1);
        }
      }
    }
  }
}
</style>
