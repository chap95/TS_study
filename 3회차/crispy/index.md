1. 아래 `x`의 타입은 `string`인가요? 아니라면, 왜 아니고, 어떻게 수정하면 될까요?
```typescript

declare function fn(x: HTMLElement): number;
declare function fn(x: HTMLDivElement): string;
declare function fn(x: any): any;

var myElem: HTMLDivElement;
var x = fn(myElem); 
```
2. 아래 `b`의 추론 타입은 무엇일까요? 왜 그럴까요?
```typescript
interface hello<T> {
  val: string;
}

interface Hallo<T> extends hello<T> {
  val: 'hallo';
}

function say<T>(x: hello<T>): T {
  // TODO: Implement
  return undefined;
}
const a: Hallo<string>
const b = say(a);
```  
3. 아래 코드는 컴파일러에게 어떤 동작을 시키나요?
```typescript
/// <reference path="moment.js" />
```
