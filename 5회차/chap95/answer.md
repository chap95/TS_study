# 5회차 정답

---

### 1. module resolution 에는 크게 2가지 방법이 있습니다. 이 두가지 방법이 무엇인지 적어주시고 이 두 가지 방법의 특징을 설멍해주세요.

##### 답 :

> classic 과 node 방법이 있다. classic 은 import를 하는 파일이 속해 있는 위치에서만 탐색을 진행하지만 node 는 import를 하는 파일 위치에서 부터 파일 디렉토리 트리를 타고 올라가며 모듈을 탐색한다는 차이가 있다.

### 2. 다음 코드를 실행할 때 module resolution 과정에 포함이 되지 않는 것을 골라주세요.

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

##### 답 : 2번

@types 폴더 아래는 index.d.ts 가 아닌 moduleB.d.ts 를 탐색합니다.

### 3. module resolution 에는 Base URL, path mapping 추가적인 flag 값들이 있습니다. 이 값들은 왜 사용하는지 작성해주세요.

##### 답 : 프로젝트 폴더를 빌드하거나 TS 가 JS로 컴파일되면은 파일 경로나 파일 이름이 변경될 수 있어서 이를 해결하기 위함
