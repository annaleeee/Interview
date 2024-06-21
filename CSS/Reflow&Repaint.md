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
  
