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