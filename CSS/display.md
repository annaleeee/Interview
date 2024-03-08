## CSS display
- display : 레이아웃을 어떻게 보여줄지 결정하는 css 속성
  
  - `display: none;`
    - 화면에서 사라짐
    - DOM에서 제거하지는 않지만, 렌더링에서 제외시킴
    - `visibility: hidden;` 과 달리 요소가 차지하는 공간조차 없앰
      
  - `display: block;`
      - 해당 영역의 줄을 전부 차지 / 줄바꿈 O
      - 태그에 따라 기본값
          - div, section, article, p, h1 등 대부분의 HTML 요소
      - width, height, margin, padding 속성 적용 가능
        
  - `display: inline;`
      - 해당 영역을 차지하고 줄바꿈없이 연속 배치
      - 컨텐츠를 딱 감싸는 정도의 크기만 갖고있음 (줄바꿈 X)
          - 컨텐츠에 맞게 크기가 자동으로 조정
              
              → width, height 적용 X / margin-top, margin-bottom도 적용 X
              
              → padding은 적용되지만, 레이아웃에 영향을 주진 않음
              
      - 태그에 따라 기본값
          - span, a, img 태그
            
  - `display: inline-block;`
      - inline + block
      - 요소자체는 inline처럼 동작해서 줄바꿈 불가능
      - 내부에서는 블록요소처럼 동작해서 크기 지정 가능
