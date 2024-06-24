## Reflow vs Repaint
** 요소가 시각적으로 변경되었을 때, 변화를 계산하여 화면에 그려주는 작업
- Reflow
  - 렌더링 엔진에서 요소를 배치하는 과정
  - 렌더 트리 구축 단계에서 DOM 트리와 스타일 규칙을 합쳐서 렌더 트리를 만들고, 여기서 reflow를 통해 각각의 요소들의 레이아웃을 위치시킴
  - 렌더 트리는 DOM 요소를 기반으로 만들어지지만, 완전히 대응되지는 않음
    - DOM 트리가 문서의 구조를 나타낸다면, 렌더 트리는 문서의 시각적 구조를 나타냄
- Repaint
  - 렌더 트리가 탐색되고 paint 메서드가 호출되어, UI 기반의 구성요소를 사용해 그리는 과정 <br>
    → reflow 작업이 이루어진 후에 repaint 작업이 이루어짐
  - 화면의 구조가 변경이 될 때는 reflow와 repaint 모두 발생함
  - 레이아웃에 영향을 주지 않는 엘리먼트 개별의 변화에 대해서는 repaint만 발생
    - color, background-color, visibility, opacity … <Br>
    → Reflow는 Repaint를 유발하지만, Repaint는 Reflow를 유발하지 않음

---

#### [ reflow가 발생하는 경우 ]
- DOM 노드의 추가, 제거
- DOM 노드의 위치 변경
- DOM 노드의 크기 변경 (margin, padding, border, width, height 등)
- CSS3 애니메이션과 트랜지션
- 폰트 변경, 텍스트 내용 변경
- 이미지 크기 변경
- offset, scrollTop, scrollLeft와 같은 계산된 스타일 정보 요청
- 페이지 초기 렌더링
- 윈도우 리사이징

#### [ reflow 최적화 ]
- 가능한 reflow 안 하는 것이 성능 측면에서 유리함 <br>
  → 비용을 발생시키는 절차이므로 (특정 요소에서 리플로우가 발생하면 주변 요소에도 영향을 주기 때문)
- 스타일을 변경할 경우 가장 하위 노드의 클래스를 변경
- 인라인 스타일 사용 X
- 애니메이션이 있는 노드는 position을 fixed 또는 absolute로 지정
  - 애니메이션 효과는 많은 reflow 비용 발생시킴
  - fixed, absolute → 지정된 노드를 전체 노드에서 분리시켜 해당 노드에서만 reflow가 발생하도록 제한시킬 수 있음
- table 레이아웃을 피한다
  - <table>은 점진적으로 렌더링 되지 않고, 모두 로드되고 테이블 너비가 계산된 후에 화면에 그려짐
- css 하위 선택자를 최소화 함
- 숨겨진 노드의 스타일을 변경한다
  - 숨겨진 노드를 표시하기 전에 노드의 컨텐츠를 먼저 변경한 후 화면에 나타내면 reflow 줄일 수 있음
- DOM 사용 최소화
  - DOM Fragment 사용 (createDocumentFragment)
- 캐시 활용
  
