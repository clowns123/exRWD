# 5일차

1. [반응형 웹 vs 적응형 웹]([https://github.com/yamoo9/cj-olive-networks/wiki/%EC%A0%81%EC%9D%91%ED%98%95-%EC%9B%B9-%EB%94%94%EC%9E%90%EC%9D%B8-VS-%EB%B0%98%EC%9D%91%ED%98%95-%EC%9B%B9-%EB%94%94%EC%9E%90%EC%9D%B8](https://github.com/yamoo9/cj-olive-networks/wiki/적응형-웹-디자인-VS-반응형-웹-디자인))
   1. 반응형은 모든기기 적용
   2. 적응형은 각각 기기마다 만들어야함
   3. 단 적응형은 리소스가 적어서 빠름
   4. 반응형은 각 기기의 모든 리소스를 가져와서 느림
2. 모바일 퍼스트 전략
   1. 모바일화면을 만들과 데스크탑을 만드는게 좋다.
3. [구글은 모바일사이트가 있으면 SEO점수가 더 높다.](https://webmasters.googleblog.com/2015/04/faqs-april-21st-mobile-friendly.html)
4.  [Google 모바일 친화성 테스트 도구](https://search.google.com/test/mobile-friendly)
5. 반응형 웹 디자인 사례
   1.  [koreawebdesign.com](http://koreawebdesign.com/tag/responsive/)
   2. [https://mediaqueri.es/](https://mediaqueri.es/)
   3.  http://responsivelogos.co.uk/
6. 반응형 웹 구현 방법
   1. 사용자 모바일 경험 고려
   2. 완성된 비주얼보다 프로토타입 테스트 우선
   3. 효율적인 네이게이션 제공 방법 고민
      1. 햄버거바 같은 디자인
   4. 이미지 최적화
   5. 모바일 기기 우선
   6. 미디어쿼리 사용법
7. 파셀, 웹팩, 바벨
   1. 파셀이 가볍다.
8. 개발버전과 배포버전은 나누자
   1. src는 개발버전
   2. dist는 배포버전
9. 적절한 사용자 입력 유도
10. 작은 모바일 화면에서도 쉽게 클릭 가능해야함
11. 타이포그래픽 최적화
12. [레진코믹스 기술블로그](https://tech.lezhin.com/)
13. 반응형 프레임워크를 사용해 프로토타이핑을 제작해보면 설계하는데 많은 시간을 절약 할 수 있습니다.
    - [Bootstrap](http://getbootstrap.com/)
    - [Foundation](https://foundation.zurb.com/)
    - [Bulma](https://bulma.io/)
    - [UI Kit](https://getuikit.com/)
    - [Semantic UI](https://semantic-ui.com/)
14. 유연한 콘텐츠
    1. 이미지같은 것을 max-widtd=100%등을 사용한다.
15. 유연한 레이아웃
    1. px보다는 %, vm, vw, rem, em, fr같이 유연하게 만든다.
16. user-scale = no는 확대가 불가능하다.
17. [미디어 쿼리 중단점](https://www.browserstack.com/guide/responsive-design-breakpoints), [부트스트랩 기준](https://getbootstrap.com/docs/4.1/layout/overview/)
18. 이미지 배율조정
    1. <img srcset 등이 있다.
19. [반응형 웹디자인 테스트](http://troy.labs.daum.net/)



# 1일차

1. 실 디바이스 테스트가 중요하다

   * 너무 하나하나 드레그를 확인하지 말자

2. http://responsivelogos.co.uk/

   * 반응형으로 잘 만들었지만 웹 접근성에서 떨어진다.

3. img에서 srcset을 사용하여 해상도에 따라 image크기를 바꿔준다.

   1. css에서도 가능하다 하지만 html에서 사용해야 성능면에서 좋다.

   2. ```html
      <a href="./index.html"><img src="./images/image-1x.png" alt="웹카페"
      srcset="./images/image-2x.png 2x,
      ./images/image-3x.png 3x"/></a>
      ```

   3. ```css
      /* 1.25 dpr */
      @media 
      (-webkit-min-device-pixel-ratio: 1.25), 
      (min-resolution: 120dpi){ 
          /* Retina-specific stuff here */
      }
      
      /* 1.3 dpr */
      @media 
      (-webkit-min-device-pixel-ratio: 1.3), 
      (min-resolution: 124.8dpi){ 
          /* Retina-specific stuff here */
      }
      
      /* 1.5 dpr */
      @media 
      (-webkit-min-device-pixel-ratio: 1.5), 
      (min-resolution: 144dpi){ 
          /* Retina-specific stuff here */
      }
      ```

4. inherit : 부모요소 상속

5. aria에는 속성과 상태가 있다.

   1. role은 속성 바뀌지 않는다.
   2. pressed, haspopup같은 상태도 있다.




<hr/>

# 2일차

>  bbc코리아가 웹 접근성을 잘 준수하였다.
>
> - aria를 잘 적용하자

* table
  * scope로 제목의 방향 설정
  * thead, tfoot은 한번만 나오지만 tbody는 여러번 나온다.
  * id/headers로 제목과 본문을 연결 가능하다.
  * ul 태그는 display: table이 되고 li태그는 display: table-cell이 된다.
  * legend태그도 normalize를 적용하면 display : table로 되기 떄문에  원하는 크기가 제대로 나오지 않는다.
    * why? normalize change table
      * Edge와 IE에서 legend에서의 텍스트를 래핑이 불가능해서(버그) table로 만든다.
  * table로는 레이아웃하지말자 gird를 쓰자
* filter
  * 다양한 효과를 낼 수 있다.
  * 그림의 뒤에 줄려면 backdrop-filter을 쓴다.
* 반응형 이미지 처리
  * max-width를 사용하자
    * 작아지면 화질이 떨어져요



<hr/>

# 3일차

1. video같은 경우에는 다양한 포맷때문에 크로스 브라우저를 생각해서 다양한 포맷을 지정하기도 한다.

   1. 하지면 최근에는 mp4를 다 지원 해준다.
   2. 자막을 꼭 넣어주자.
      1. 클로즈 자막과 오픈 자막 형식이 있다.
         1. 클로즈는 영상 안에 있는 것
         2. 오픈은 껐다 켰다 하는 것
         3. vtt포맷

2. iframe는 높이를 가지지 못한다.

   1. 그렇기 때문에 반응형으로 만들려면 div로 감싸주고 width와 padding-bottom으로 높이를 준다.
      1. 높이가 너비를 기준으로 줄어들게 하고싶다.
      2. padding의 %는 너비를 기준으로 한다.
      3. padding으로 높이를 주면 너비에 따라 높이가 줄어든다.
   2. iframe을 안에 넣고 pos:a으로 offset는 left:0 top:0으로 해준다.
   3.  div를 pos:r을 해주고 크기를 100%를 준다.

3. counter-increment로 꾸밀 수 있는 숫자를 넣을 수 있다.

4. css에서도 변수를 사용할 수 있다.

   1. ```css
      :root {
        --main-bg-color: pink;
      }
      
      body {
        background-color: var(--main-bg-color);
      }
      ```

5. 반응형은 감싸는 박스의 크기가 고정이여도 안쪽 요소를 가변적인값을 주면 반응형으로 만들기 쉽다.





















