---

(1~3번) 다음 예시 tsconfig를 보고, 상황에 알맞은 해결책을 제시해주세요.

```typescript
{
   "compilerOptions": {
     "module": 'commonjs'
   },
   "files": [
     'main.ts'
   ]
}
```

1. 아래 코드 조각에서 발생하는 에러를 해결하기 위해선, tsconfig파일을 수정하는 방법이 있습니다. 어떤 부분을 수정해야 될까요?

```typescript
// say hello.ts
import { hello } from 'moduleA'

export function sayHello() {
  console.log(hello);
}

// 발생한 에러
TS2307: Cannot find module 'moduleA'
```

2. `main.ts`파일과 `sub.ts`파일을 컴파일 하고자 합니다. 아래와 같은 명령어를 커멘드라인에 입력한 경우, `sub.ts` 파일만 컴파일이 됩니다. 왜 그렇고, 어떻게 명령어를 고치면 될까요?
```shell
tsc sub.ts
```

3. 위 컴파일러 옵션을 수정하여 `ES2015`의 `Map`을 사용할 수 있도록 변경하는 방법을 알려주세요.

---

4. 아래에 제시된 상황들 중 컴파일러 옵션의 `strict`옵션으로 확인이 불가한 상황을 골라주세요.

    1. null과 관련된 에러가 계속 발생합니다.
    1. 클래스의 초기화 되지않은 프로퍼티로 인해 오류가 계속 발생합니다.
    1. switch문에서 case에 break/return을 하지 않는 실수가 발생합니다.
    1. class 에서 this가 global object를 가리킵니다.
