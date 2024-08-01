## console.log vs process.stdout.write 
- `console.log` 사용
  - 출력할 때마다 개행 <br>
  ``` jsx
  console.log("자바");
  console.log("스크");
  console.log("립트");
  ↓
  자바
  스크
  립트
  ```
- `process.stdout.write` 사용
  - 개행 X
  ``` jsx
  process.stdout.write("자바");
  process.stdout.write("스크");
  process.stdout.write("립트");
  ↓
  자바스크립트
  ```
