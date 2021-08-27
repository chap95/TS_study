(1 ~ 3번)시나리오

오픈 소스로 댓글 서비스를 만들고 있습니다.

댓글은 아래와 같은 데이터 구조로 이루어져 있습니다.

``` typescript

interface IComment {
  id: number;
  createdAt: string;
  updatedAt: string;
  contents: Contents;
  author: IAuthor;
  relatedCategory: string | number;
  parentCommentId: number;
}

```

이 데이터 구조로 다중 대댓글이 가능한 서비스를 만들고자 합니다. 아래 제시되는 문제들의 해결 방법을 하나 이상 제시해 주세요.

---

1. `relatedCategory`가 1개 이상인 경우를 대비해야 합니다. interface 예시를 하나 작성해 주세요.

1. 대댓글의 개수를 보여주는 기능이 기획되었습니다. 어떤 순서로 인덱싱을 해두면 빠르게 찾을 수 있을까요?

1. `IComment`에서 아래 속성만을 사용하고자 합니다. type 예시 하나를 작성해 주세요.

    ```
    createdAt | contents | relatedCategory
    ```

---
(4 ~ 5)코드조각
``` typescript
// const assertion

let books = [
  {
    name: '알고리즘 문제 해결 전략 2'
  }, 
  {
    name: '생활속의 회계'
  }
] as const;

// enum

enum Color {
  red = 'red',
  blue = 'blue',
  green = 'green',
}

```

4. 위 코드 조각에서 const assertion에 해당하는 코드조각의 타입추론 결과를 작성해 주세요.


5. 위 코드 조각에서 Color를 enum으로 작성하였습니다. 해당 enum은 const assertion으로도 작성이 가능합니다.
    어떤 방식이 왜 더 좋은 방법일지 설명해 주세요.
    (단, tsconfig의 compiler option에 --isolatedModules 플래그가 true임을 가정합니다.)
