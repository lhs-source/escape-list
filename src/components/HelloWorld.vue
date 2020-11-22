<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1>
    <h2>{{msg2}}</h2> -->
    <!-- <div class="escape-item" v-for="(value, name) of escapeList" v-bind:key="name"> 
      <span class="title">{{name}}</span> 
      <span class="value">{{value}}</span>
    </div> -->
    
    <div style="display: grid; grid-template-columns: repeat(4, 1fr);">
      
    <!-- <div> -->
      <div class="escape-item" v-for="(item) of escapeList" v-bind:key="item.name"> 
        <a :href="item.url" target="_blank">
          <div>
            <img class="poster" :src="item.img">
            <p>
              <span class="title">{{item.name}}</span> 
              <span class="value">{{item.rate}}</span>
            </p>
            <p>
              <span class="location">{{item.location}}</span>
            </p>
          </div>
        </a>
      </div>
    </div>
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

  escapeList = [{'name': '싸이코메트리(감독판)', 'rate': 4.0, 'location': '이스케이퍼스 1호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php?theme=452', 'img': 'https://yologuys.com/Escape_img/theme/452.jpg'}, {'name': '포츈 테라피', 'rate': 3.7, 'location': '이스케이프 샾', 'url': 'https://www.roomescape.co.kr/theme/detail.php?theme=3261', 'img': 'https://yologuys.com/Escape_img/theme/3261.jpg'}, {'name': 'LOST KINGDOM : 잊혀진 전설', 'rate': 3.7, 'location': '비트포비아 강남던전', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2018', 'img': 'https://yologuys.com/Escape_img/theme/2018.jpg'}, {'name': '커튼콜', 'rate': 3.9, 'location': '넥스트에디션 건대2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1836', 'img': 'https://yologuys.com/Escape_img/theme/1836.jpg'}, {'name': '시크릿 에이전트', 'rate': 3.6, 'location': '룸즈에이 대학로점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=514', 'img': 'https://yologuys.com/Escape_img/theme/514.jpg'}, {'name': '어웨이큰', 'rate': 3.8, 'location': '마스터키 강남프라임점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3329', 'img': 'https://yologuys.com/Escape_img/theme/3329.jpg'}, {'name': '소식', 'rate': 3.9, 'location': '뉴 이스케이프 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3065', 'img': 'https://yologuys.com/Escape_img/theme/3065.jpg'}, {'name': 'Tempo Rubato', 'rate': 4.8, 'location': '디코더', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3206', 'img': 'https://yologuys.com/Escape_img/theme/3206.jpg'}, {'name': '방탈출 아카데미 (Normal과정)', 'rate': 3.6, 'location': '넥스트에디션 건대2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3092', 'img': 'https://yologuys.com/Escape_img/theme/3092.jpg'}, {'name': '자비원', 'rate': 4.0, 'location': '비트포비아 히든퀘스트 2', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=599', 'img': 'https://yologuys.com/Escape_img/theme/599.jpg'}, {'name': '동창회', 'rate': 4.3, 'location': '머더파커 건대2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3306', 'img': 'https://yologuys.com/Escape_img/theme/3306.jpg'}, {'name': '기이한 라커룸', 'rate': 3.6, 'location': '언리미티드 이스케이프', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2122', 'img': 'https://yologuys.com/Escape_img/theme/2122.jpg'}, {'name': '인형괴담', 'rate': 3.7, 'location': '미스터리 룸 이스케이프 강남점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=67', 'img': 'https://yologuys.com/Escape_img/theme/67.jpg'}, {'name': '첫 출근 이야기', 'rate': 4.5, 'location': '오늘, 탈출', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3046', 'img': 'https://yologuys.com/Escape_img/theme/3046.jpg'}, {'name': '프레임 하이커', 'rate': 3.7, 'location': '룸즈에이 부산서면점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1507', 'img': 'https://yologuys.com/Escape_img/theme/1507.jpg'}, {'name': '화이트룸', 'rate': 4.2, 'location': '마스터키 천안두정점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1112', 'img': 'https://yologuys.com/Escape_img/theme/1112.jpg'}, {'name': '그카지말라캤자나', 'rate': 4.2, 'location': '키이스케이프 강남점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=144', 'img': 'https://yologuys.com/Escape_img/theme/144.jpg'}, {'name': '외출 : 나가서 놀고싶다.', 'rate': 3.8, 'location': '하일 이스케이프', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3332', 'img': 'https://yologuys.com/Escape_img/theme/3332.jpg'}, {'name': 'EP1 : 시간이 멈춘 마을', 'rate': 4.3, 'location': '포인트 나인', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3312', 'img': 'https://yologuys.com/Escape_img/theme/3312.jpg'}, {'name': '코리안 타임', 'rate': 3.9, 'location': '그레이트 이스케이프', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3247', 'img': 'https://yologuys.com/Escape_img/theme/3247.jpg'}, {'name': 'Make-up', 'rate': 3.6, 'location': '넥스트에디션 건대2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1909', 'img': 'https://yologuys.com/Escape_img/theme/1909.jpg'}, {'name': '시크릿제트', 'rate': 4.0, 'location': '제트방탈출카페', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1530', 'img': 'https://yologuys.com/Escape_img/theme/1530.jpg'}, {'name': '명당', 'rate': 4.7, 'location': '숨바꼭질 2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3340', 'img': 'https://yologuys.com/Escape_img/theme/3340.jpg'}, {'name': '전생연분', 'rate': 4.5, 'location': '러시아워', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3268', 'img': 'https://yologuys.com/Escape_img/theme/3268.jpg'}, {'name': '무채색 인간', 'rate': 3.9, 'location': '솔버 2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2185', 'img': 'https://yologuys.com/Escape_img/theme/2185.jpg'}, {'name': '파커vs파커', 'rate': 3.8, 'location': '머더파커 대구점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1901', 'img': 'https://yologuys.com/Escape_img/theme/1901.jpg'}, {'name': '인연', 'rate': 4.0, 'location': '방탈출카페 숨바꼭질', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2165', 'img': 'https://yologuys.com/Escape_img/theme/2165.jpg'}, {'name': '트레져헌터', 'rate': 3.9, 'location': '룸엘이스케이프 신림점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3138', 'img': 'https://yologuys.com/Escape_img/theme/3138.jpg'}, {'name': 'Do The G', 'rate': 3.6, 'location': '마스터키 강남프라임점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3331', 'img': 'https://yologuys.com/Escape_img/theme/3331.jpg'}, {'name': '필활', 'rate': 4.0, 'location': '룸즈에이 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1892', 'img': 'https://yologuys.com/Escape_img/theme/1892.jpg'}, {'name': 'LOST KINGDOM 2 : 대탐험의 시작', 'rate': 4.3, 'location': '비트포비아 강남 던전II', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3355', 'img': 'https://yologuys.com/Escape_img/theme/3355.jpg'}, {'name': '극', 'rate': 3.9, 'location': '넥스트에디션 신림점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3178', 'img': 'https://yologuys.com/Escape_img/theme/3178.jpg'}, {'name': '리디아의 사자', 'rate': 3.7, 'location': '뉴 이스케이프 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3136', 'img': 'https://yologuys.com/Escape_img/theme/3136.jpg'}, {'name': '뽀득뽀득', 'rate': 3.7, 'location': '룸즈에이 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2060', 'img': 'https://yologuys.com/Escape_img/theme/2060.jpg'}, {'name': '귀향', 'rate': 4.0, 'location': '문이스케이프', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1790', 'img': 'https://yologuys.com/Escape_img/theme/1790.jpg'}, {'name': '도시괴담 Part.1 ‘The Day of Horror’', 'rate': 3.6, 'location': '마스터키 강남점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=153', 'img': 'https://yologuys.com/Escape_img/theme/153.jpg'}, {'name': '한잔해', 'rate': 3.8, 'location': '뉴 이스케이프 광주점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1728', 'img': 'https://yologuys.com/Escape_img/theme/1728.jpg'}, {'name': '에이전트 스노우', 'rate': 3.7, 'location': '에픽플랜 건대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3264', 'img': 'https://yologuys.com/Escape_img/theme/3264.jpg'}, {'name': '녀', 'rate': 4.2, 'location': '러시아워', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3288', 'img': 'https://yologuys.com/Escape_img/theme/3288.jpg'}, {'name': '출생', 'rate': 4.0, 'location': '에픽플랜 건대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3263', 'img': 'https://yologuys.com/Escape_img/theme/3263.jpg'}, {'name': '왕자님이 찾으십니다', 'rate': 3.8, 'location': '룸즈에이 강남점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3338', 'img': 'https://yologuys.com/Escape_img/theme/3338.jpg'}, {'name': '금잔화', 'rate': 3.8, 'location': '플레이 이스케이프 원주점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3297', 'img': 'https://yologuys.com/Escape_img/theme/3297.jpg'}, {'name': '구룡 잠들지 않는 도시', 'rate': 4.1, 'location': '비트포비아 대학로점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3346', 'img': 'https://yologuys.com/Escape_img/theme/3346.jpg'}, {'name': '대대대대대대대대대탈출', 'rate': 3.6, 'location': '비밀의화원 동성로점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2174', 'img': 'https://yologuys.com/Escape_img/theme/2174.jpg'}, {'name': '유럽횡단 야간열차', 'rate': 3.9, 'location': '서울 이스케이프 룸 강남 1호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=93', 'img': 'https://yologuys.com/Escape_img/theme/93.jpg'}, {'name': '만약, 당신이 길을 잃었다면', 'rate': 4.2, 'location': '이스케이퍼스 2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3243', 'img': 'https://yologuys.com/Escape_img/theme/3243.jpg'}, {'name': '졸업', 'rate': 4.0, 'location': '싸인 이스케이프 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3161', 'img': 'https://yologuys.com/Escape_img/theme/3161.jpg'}, {'name': '성역전설', 'rate': 3.6, 'location': '제로월드 김포점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1974', 'img': 'https://yologuys.com/Escape_img/theme/1974.jpg'}, {'name': '김파커 끝없는 복수', 'rate': 3.6, 'location': '머더파커 E.T 3호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1605', 'img': 'https://yologuys.com/Escape_img/theme/1605.jpg'}, {'name': '나비효과', 'rate': 3.7, 'location': '제로월드 강남점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3319', 'img': 'https://yologuys.com/Escape_img/theme/3319.jpg'}, {'name': '고백', 'rate': 4.5, 'location': '키이스케이프 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1784', 'img': 'https://yologuys.com/Escape_img/theme/1784.jpg'}, {'name': '화이트룸', 'rate': 4.0, 'location': '넥스트에디션 신촌점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=276', 'img': 'https://yologuys.com/Escape_img/theme/276.jpg'}, {'name': '아뜰리에', 'rate': 3.7, 'location': '비밀의화원 부산서면점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1750', 'img': 'https://yologuys.com/Escape_img/theme/1750.jpg'}, {'name': '책 읽어주는 남자', 'rate': 3.7, 'location': '비트포비아 미션브레이크 CGV 광주금남로점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2098', 'img': 'https://yologuys.com/Escape_img/theme/2098.jpg'}, {'name': '히어로 아카데미', 'rate': 3.7, 'location': '룸즈에이 부산서면점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1508', 'img': 'https://yologuys.com/Escape_img/theme/1508.jpg'}, {'name': '마카오:꼭두각시 광시곡', 'rate': 3.8, 'location': '룸익스케이프 화이트점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=270', 'img': 'https://yologuys.com/Escape_img/theme/270.jpg'}, {'name': '제이콥', 'rate': 4.1, 'location': '트릭', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3208', 'img': 'https://yologuys.com/Escape_img/theme/3208.jpg'}, {'name': '뱀파이어 헌터', 'rate': 4.0, 'location': '마스터키 건대로데오점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3341', 'img': 'https://yologuys.com/Escape_img/theme/3341.jpg'}, {'name': '죽음을 부르는 재즈바', 'rate': 3.7, 'location': '서울 이스케이프 룸 부평점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1030', 'img': 'https://yologuys.com/Escape_img/theme/1030.jpg'}, {'name': '골드러시', 'rate': 3.6, 'location': '카오스 이스케이프 2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1942', 'img': 'https://yologuys.com/Escape_img/theme/1942.jpg'}, {'name': '키메이커', 'rate': 4.1, 'location': '룸즈에이 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1793', 'img': 'https://yologuys.com/Escape_img/theme/1793.jpg'}, {'name': '화생설화 : Blooming', 'rate': 4.4, 'location': '비트포비아 던전101', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3320', 'img': 'https://yologuys.com/Escape_img/theme/3320.jpg'}, {'name': '동화나라 수비대', 'rate': 3.8, 'location': '넥스트에디션 건대2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1896', 'img': 'https://yologuys.com/Escape_img/theme/1896.jpg'}, {'name': '메이즈 헌터', 'rate': 3.6, 'location': 'G9 이스케이프', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1456', 'img': 'https://yologuys.com/Escape_img/theme/1456.jpg'}, {'name': '일주(ONE WEEK)', 'rate': 3.8, 'location': '머더파커 전주1호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3113', 'img': 'https://yologuys.com/Escape_img/theme/3113.jpg'}, {'name': '몬스터 : 10800', 'rate': 3.9, 'location': '넥스트에디션 건대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=168', 'img': 'https://yologuys.com/Escape_img/theme/168.jpg'}, {'name': '멍스타그램', 'rate': 3.9, 'location': '이스케이퍼스 2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2229', 'img': 'https://yologuys.com/Escape_img/theme/2229.jpg'}, {'name': '더 케이지', 'rate': 3.6, 'location': '솔버', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=185', 'img': 'https://yologuys.com/Escape_img/theme/185.jpg'}, {'name': '비밀의 모험', 'rate': 3.7, 'location': '비밀의화원 혜화점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1890', 'img': 'https://yologuys.com/Escape_img/theme/1890.jpg'}, {'name': '스물아홉', 'rate': 3.7, 'location': '비밀의화원 포레스트점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3265', 'img': 'https://yologuys.com/Escape_img/theme/3265.jpg'}, {'name': 'SHIT', 'rate': 3.6, 'location': '마스터키 광주점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1833', 'img': 'https://yologuys.com/Escape_img/theme/1833.jpg'}, {'name': '날씨의 신', 'rate': 3.9, 'location': '비트포비아 서면던전', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3001', 'img': 'https://yologuys.com/Escape_img/theme/3001.jpg'}, {'name': '빛과 그림자', 'rate': 3.7, 'location': '셜록홈즈 인천논현점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1985', 'img': 'https://yologuys.com/Escape_img/theme/1985.jpg'}, {'name': '거상', 'rate': 4.4, 'location': '싸인 이스케이프 홍대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2188', 'img': 'https://yologuys.com/Escape_img/theme/2188.jpg'}, {'name': '호그와트 - 후플푸프', 'rate': 3.9, 'location': '더클루 신촌프리미엄점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2192', 'img': 'https://yologuys.com/Escape_img/theme/2192.jpg'}, {'name': '디어 마르시', 'rate': 4.2, 'location': '솔버 2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=253', 'img': 'https://yologuys.com/Escape_img/theme/253.jpg'}, {'name': '네드', 'rate': 4.7, 'location': '키이스케이프 강남더오름점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2197', 'img': 'https://yologuys.com/Escape_img/theme/2197.jpg'}, {'name': '하루끝', 'rate': 4.4, 'location': '러시아워', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3324', 'img': 'https://yologuys.com/Escape_img/theme/3324.jpg'}, {'name': '레드룸', 'rate': 3.9, 'location': '다이아에그', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1394', 'img': 'https://yologuys.com/Escape_img/theme/1394.jpg'}, {'name': '단잠', 'rate': 4.3, 'location': '셜록홈즈 잠실2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=2008', 'img': 'https://yologuys.com/Escape_img/theme/2008.jpg'}, {'name': '디스맨', 'rate': 4.3, 'location': '넥스트에디션 부평점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1057', 'img': 'https://yologuys.com/Escape_img/theme/1057.jpg'}, {'name': '탈옥 : 특별수용 소', 'rate': 4.0, 'location': '제로월드 김포점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3143', 'img': 'https://yologuys.com/Escape_img/theme/3143.jpg'}, {'name': '라스트 잡', 'rate': 3.9, 'location': '비밀의화원 포레스트점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3246', 'img': 'https://yologuys.com/Escape_img/theme/3246.jpg'}, {'name': '타짜', 'rate': 4.0, 'location': '서울 이스케이프 룸 강남 2호 점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1760', 'img': 'https://yologuys.com/Escape_img/theme/1760.jpg'}, {'name': '비밀의 가족', 'rate': 3.8, 'location': '비밀의화원 미드나잇점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3104', 'img': 'https://yologuys.com/Escape_img/theme/3104.jpg'}, {'name': '팩토리 엠', 'rate': 3.8, 'location': '비밀의화원 미드나잇점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3137', 'img': 'https://yologuys.com/Escape_img/theme/3137.jpg'}, {'name': '타짜', 'rate': 3.7, 'location': '더코드 한신포차점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3116', 'img': 'https://yologuys.com/Escape_img/theme/3116.jpg'}, {'name': '괴도루키', 'rate': 3.6, 'location': '셜록홈즈 일산점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1986', 'img': 'https://yologuys.com/Escape_img/theme/1986.jpg'}, {'name': '동물병원', 'rate': 3.6, 'location': '머더파커 건대2호점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3309', 'img': 'https://yologuys.com/Escape_img/theme/3309.jpg'}, {'name': '신비의 숲-고대 마법의 비밀', 'rate': 3.6, 'location': '키이스케이프 부산점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1500', 'img': 'https://yologuys.com/Escape_img/theme/1500.jpg'}, {'name': 'Tester', 'rate': 3.7, 'location': '넥스트에디션 신림점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=3125', 'img': 'https://yologuys.com/Escape_img/theme/3125.jpg'}, {'name': '다시 봄', 'rate': 3.9, 'location': '넥스트에디션 건대점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=171', 'img': 'https://yologuys.com/Escape_img/theme/171.jpg'}, {'name': '큐브', 'rate': 3.6, 'location': '코드네임 블랙 부산점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1472', 'img': 'https://yologuys.com/Escape_img/theme/1472.jpg'}, {'name': 'GATE : CCZ (episode 1)', 'rate': 4.1, 'location': '싸인 이스케이프 인계점', 'url': 'https://www.roomescape.co.kr/theme/detail.php/?theme=1789', 'img': 'https://yologuys.com/Escape_img/theme/1789.jpg'}];
  
  created(){
    console.log("create HelloWorld");

    this.escapeList.sort((a, b)=>{
      return a.rate > b.rate ? -1 : 1;
    });
  }

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
  text-decoration: none;
  color:inherit;
}
p{
  margin:0;
}

.escape-item{
  padding: 8px;
  /* background-color: #eee; */
  cursor: pointer;
  transition:300ms;
}
.escape-item:hover{
  background-color: rgb(165, 190, 167);
  transition:100ms;
}
.escape-item:hover > .value{
  transition:100ms;
  text-shadow: 2px 2px 3px rgb(255, 255, 255);
}
.escape-item:hover > .title{
  transition:100ms;
  text-shadow: 2px 2px 3px rgb(255, 255, 255);
}
.poster{
  transition:100ms;
  height:108px;
  margin:0 4px;
}
.poster:hover{
  transition:100ms;
  -webkit-transform: scale(5);
}
.title{
  font-weight: 600; 
  font-size:1.4em;
}
.value{
  font-weight: 700;
  font-size:2em; 
  margin:0 4px; 
  color:goldenrod;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: rgb(99, 74, 12);
  
  transition:200ms;
}
.location{
  font-weight: 600; 
  /* font-size:1.2em; */
}
</style>
