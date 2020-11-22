<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{msg2}}</h2>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-typescript" target="_blank" rel="noopener">typescript</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    msg: String,
    msg2 : String,
  }
})
export default class HelloWorld extends Vue {
  msg!: string
  msg2!: string

  escapeList = {'오씨네 장난감 가게': 3.7, '신의 여인들': 3.9, '히로인': 3.6, '평촌 이세계': 3.6, '키메이커': 4.1, '죽음을 부르는 재즈바': 3.7, '싸이코메트리(감독판)': 4.0, '그래도 피망은 먹기 싫단 말이에욧': 3.8, 'Tempo Rubato': 4.8, '알카트라즈 지하감옥': 3.8, 'EP2 : 열쇠공의 이중생활': 4.6, '종갓집 민씨': 3.6, '타인은 지옥이다': 4.1, '화이트룸': 4.2, '너의곁으로': 3.9, '집으로': 3.7, '안산 코노': 4.5, '디스토피아': 4.5, '산장 : 사라진 목격자': 4.1, '에이전트 스노우': 3.7, '학교<야자탈출>': 4.1, 'CIA본부에서의 탈출': 3.8, '엔제리오': 4.6, '극': 3.9, '동물병원': 3.6, '비밀의 모험': 3.7, '기이한 라커룸': 3.6, '이스케이프 플랜': 4.2, '단잠': 4.3, 'METRO': 4.2, '에이전트 : 노출된 미션': 3.7, '기다려, 금방 갈게': 3.9, '냥이강쥐의 대모험': 4.0, '나홀로 집에': 3.6, '대감댁변씨': 3.9, '명당': 4.7, '인형괴담': 4.2, '파커4': 4.4, '파커vs파커': 3.8, '디데이': 3.7, '크리쳐 - 신인류의 탄생': 3.6, 'EP1 : 시간이 멈춘 마을': 4.3, '8585세탁소': 3.6, '사라진 보물 : 대저택의 비밀': 3.6, 'LIVE': 3.9, '죽음의 신': 3.9, '무죄': 3.9, '시크릿제트': 4.0, '해커:The code breaker': 3.6, '주희다방': 3.6, '칠칠': 4.5, '여행': 4.2, '금잔화': 3.8, '레드룸': 3.9, '주차장': 3.6, '타짜': 3.7, '광야': 3.9, '오늘, 나는': 4.1, '고백': 4.5, '디코이': 4.1, '블랙데이': 3.6, '암행': 3.9, '방탈출 아카데미 (Master과정)': 4.1, '그리고 아무도 없었다': 3.8, '하루끝': 4.4, '마카오:꼭두각시 광시곡': 3.8, '그카지말라캤자나': 4.2, '루시드 드림': 3.8, '전래동 자살사건': 4.4, '셜록-죽음의 전화': 3.6, '브로커 나씨': 3.6, 'Furious Revenge(남자방)': 3.6, '내 이름 지배만': 3.7, '평범한 하루': 4.0, 'Tester': 3.7, '어제, 그리고 오늘': 4.0, '몬스터 : 10800': 3.9, '소식': 3.9, '추적': 3.7, '꿈의 공장': 4.0, '낭랑카페': 4.1};
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
