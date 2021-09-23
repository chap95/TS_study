# 3주차 문제

- 다음 예제코드를 본 후 물음에 답하시오.

```
declare module '*.gif' {
  const content: StaticImageData

  export default content
}
```

#### 1. 위 코드를 설명해주세요. (declare module 중심으로)

#### 2. 위 예제 코드와 아래에 나온 코드의 차이점을 말해주세요.

```
declare namespace gif {
  const content: StaticImageData

  export default content
}
```

#### 3. 타입스크립트의 namespace 는 JS 의 어떠한 문제를 해결하기 위해 만들어졌나요?
