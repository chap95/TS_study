### 4주차 문제입니다.

---

다음 코드와 관련된 3문제를 해결해주세요.

```js
function Person(first, last, age, gender, interests, onBye) {
  this.first = first;
  this.last = last;
  this.age = age;
  this.gender = gender;
  this.interests = interests;
  this.onBye = onBye;

  const person1 = new Person(
    "Bob",
    "Smith",
    32,
    "male",
    ["music", "skiing"],
    () => {
      console.log("bye bye!!");
    }
  );
  const person2 = new Person(
    "Tom",
    "Eden",
    30,
    "male",
    ["soccer", "game"],
    () => {
      console.log("bye bye!!");
    }
  );
}
```

##### 1. 위코드에서 다음 제시되는 코드를 실행했을 때 예측되는 결과 값을 말해주세요.

```
console.log(person1.__proto__);
console.log(Person.prototype);
console.log(person1.__proto__.constructor);
console.log(Person.constructor);
```

##### 2. 다음 제시되는 코드의 메소드 생성방식과 위 코드에서의 메소드 생성방식의 차이점을 설명해주세요.

```js
Person.prototype.onBye = function () {
  console.log("bye bye!!");
};
```

##### 3. 2번 방식으로 생성된 메소드를 console.log 에 찍어내는 코드를 작성해주세요.

##### 4. JS에서는 객체를 만드는 방법이 다양합니다. 각 방법은 근소한 차이가 존재하지만 공통점이 있습니다. 이 공통점이 어떤것인지 설명해주세요. (메소드 관점으로)
