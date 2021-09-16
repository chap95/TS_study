1. 
  ```typescript
    foo, constructor, [[prototype]]
  ```

1. 일반적으로 속성에 대한 접근을 시도할 경우, prototype chain을 따라 속성의 존재 유무를 검사합니다. 이는 때로 성능 저하를 불러일으킬 수 있습니다. hasOwnProperty를 이용하면, prototype chain을 따라가지 않고, 검사한 오브젝트에 대해서만 참조하게 됩니다. 따라서 성능 저하가 발생할 정도로 상속이 깊게 된 경우, hasOwnProperty를 사용할 수 있습니다.

1. 위임형 상속, 연결형 상속, 함수형 상속.

# 참조 사이트
[MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
