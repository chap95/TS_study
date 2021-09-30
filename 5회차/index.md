아래 모든 문제는 webpack을 기준으로 작성되었습니다. 

1. 아래 directory 구조에서 'hello.ts'의 'moduleA'는 어떤 버전을 참조하게 될까요?

  ``` typescript
  // hello.ts
  import {hello} from 'moduleA'

  console.log(hello());
  ```

  ```c
  // directory 구조
  - src
    - package.json: moduleA - 1.1.1
    - say
      - package.json: moduleA - 1.2.1
      - hello.ts
  ```

  2. 절대 경로로 모듈을 참조하기 위해서 tsconfig.json의 어떤 옵션을  에서 설정하면 되나요?

  3. 절대 경로로 모듈을 참조하기 위해서 webpack.config.js의 어떤 옵션을  에서 설정하면 되나요?
