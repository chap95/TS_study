# 5주차 문제

---

> 1.  module resolution 에는 크게 2가지 방법이 있습니다.
>     이 두가지 방법이 무엇인지 적어주시고 이 두 가지 방법의 특징을 설멍해주세요.

> 2.  다음 코드를 실행할 때 module resolution 과정에
>     포함이 되지 않는 것을 골라주세요.

```typescript
// 현재 파일의 위치 -> /root/src/moduleA.ts
import { b } from "moduleB";
```

아래는 보기

```
1. /root/src/node_modules/moduleB/index.d.ts
2. /root/src/node_modules/@types/index.d.ts
3. /node_modules/moduleB/index.d.ts
```

> 3.  module resolution 에는 Base URL, path mapping 추가적인 flag 값들이 있습니다. 이 값들은 왜 사용하는지 작성해주세요.
