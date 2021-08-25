# 1회차 문제

---

1 ~ 6 O,X 문제

###### 1. JS 에서 원시 타입은 immutable 이다.

###### 2. JS 에서 void 는 원시 타입에 해당한다.

###### 3. JS 에서 finally 키워드는 Promise 가 fulfilled 되었을 때만 동작한다.

###### 4. JS 에서는 mutable 한 객체도 immutable 하게 변경할 수 있다.

###### 5. 웹 브라우저에서 전역 객체는 window 이다.

###### 6. JS 에서 this 는 lexical scope 를 가진다.

7 ~ 9 코드 실행결과 맞추기

###### 7.

```
console.log("0" == 0);
console.log(0 == []);
console.log("0" == []);
```

###### 8.

```
var obj = {
  bar: function() {
    var x = (() => this);
    return x;
  }
};

var fn = obj.bar();

console.log(fn() === obj);
console.log(fn2()() === obj);
```

###### 9.

```
console.log('A');
setTimeout(function() {
   console.log('B');
}, 0);
var promise = new Promise(function(resolve, reject) {
   resolve();
});
promise.then(function(resolve) {
   console.log('C');
})
.then(function(resolve) {
   console.log('D');
});
console.log('E');
```

###### 10. 자바스크립트 String() 과 .toString() 의 차이점을 서술해주세요.
