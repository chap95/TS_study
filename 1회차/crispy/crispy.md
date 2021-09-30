1. 
``` typescript

interface IMultiCategoryComment extends Omit<IComment, 'relatedCategory'> {
  relatedCategory: (string | number)[] | string | number;
}

```

2.

relatedCategory -> parentCommentId

더 큰 개념이라서, indexing 진행시 최초 index table의 크기가 더 작아집니다.

3. 

```typescirpt
  type temp = Pick<IComment, 'createdAt' | 'contents' | 'relatedCategory'>
```

4. 
```typescript

let books: readonly [
  {
    readonly name: '알고리즘 문제 해결 전략 2'
  }, 
  {
    readonly name: '생활속의 회계'
  }
]
```

5.

const assertion으로 작성하는게 더 좋습니다.

1. enum 타입은 tree shaking이 어렵습니다.
    enum의 트랜스 파일 결과는 IIFE로, 사용여부 판단이 어려워 tree shaking이 안됩니다.
1. const enum의 경우도 마찬가지 입니다.
    isolatedModules 플래그가 true일 경우, export된 결과는 일반 enum과 같으므로, 전자가 좋습니다.
1. 안정적입니다.
    
    enum은 아래와 같은 상황이 일어날 수 있습니다. 만일, color를 number code로 저장할 경우에는 문제가 발생할 수 있습니다.
    ``` typescript
    enum Ho {
      a = 1,
      b = 2,
    }

    const val: Ho = 2 // error
    ```

참조
1. TypeScript enum을 사용하지 않는 게 좋은 이유를 Tree-shaking 관점에서 소개합니다.
https://engineering.linecorp.com/ko/blog/typescript-enum-tree-shaking/
1. 안녕, TypeScript enum | Kabuku Developers Blog(일본어)
https://www.kabuku.co.jp/developers/good-bye-typescript-enum
1. https://www.typescriptlang.org/docs/handbook/release-notes/typescript-3-4.html