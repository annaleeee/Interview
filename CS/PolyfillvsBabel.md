## Pollyfill과 Babel
- 폴리필 (Pollyfill)
  - 현재 브라우저에서 지원하지 않는 최신 기능이나 API를 구현하여, 이전 브라우저에서도 해당 기능을 사용할 수 있도록 해주는 코드 조각
  - 브라우저에서 지원하지 않는 코드를 사용 가능한 코드 조각이나 플러그인으로 변환한 코드
      
      (→ 브라우저가 이해할 수 없는 코드에 대하여, 이해할 수 있는 코드 소스를 제공)
        
##### [ 바벨과의 차이점 ]
- 변경된 표준을 준수할 수 있도록 기존 함수의 동작 방식을 수정하거나 새롭게 구현 → 누락된 새로운 기능을 메꿔주는 역할

---

- 바벨 (Babel)
   - 바벨은 ESNext에서 지원하는 문법을 ES5 문법으로 번역
    - `Babel is a JavaScript compiler`
    - 바벨에 의해 컴파일될 수 있는 새로운 문법
        - arrow function, class, template literal, const/let
    - 바벨에 의해 컴파일될 수 없고, 폴리필이 필요한 문법
        
        (→ ES5의 global namespace( window )에 존재 X → 번역 불가능)
        
        [ 표준 내장 객체 및 메서드 ]
        
        - 새로운 객체 ( `Promise`, `Set`, `Map`, ... )
        - 새로운 메서드 ( `Array.prototype.includes`, `Object.assign()` ,... )
        - 새로운 함수 ( `fetch`, ... )
        
        → polyfill 사용 ⇒ Map, Promise, Set 등을 사용 가능한 객체로 만들어 줌
