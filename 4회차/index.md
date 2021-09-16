1. 다음 코드를 실행할 경우, console에 출력된 오브젝트가 가지는 속성을 말해주세요. 기준은 chrome입니다.
  ```typescript
    function doSomething(){}
    doSomething.prototype.foo = "bar";
    console.log( doSomething.prototype );
  ```

1. 프로토타입의 속성 검사를 hasOwnProperty로 하게됩니다. 일반 속성 접근과의 차이를 설명해 주세요.

1. 프로토타입의 상속 방법 3가지를 작성해 주세요.