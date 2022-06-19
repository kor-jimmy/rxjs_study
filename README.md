## RxJS

#### 반응형 프로그래밍을 위해 만들어진 Reactive X

- RxJava, RxJS, Rx.NET, UniRX(C# Unity), RxLua, RxRuby, RxGo, RxKotlin, RxSwift ..
- 다양한 언어에서 사용 가능한 Library

#### RxJS와 찰떡 궁합인 Functional Programming

- 코딩중 오류를 일으킬 수 있는 변수의 사용을 지양하고 순수함수를 사용
- (X) Variables (O) Pure Functions

#### 일반적인 프로그래밍

```
아래 숫자 배열 중 짝수 중에 첫 3개의 값을 제곱하여 한 문자열로 합치기

const numbers = [
 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
]
let count = 0;
let result = '';
for(let i=0; i < numbers.length -1 && count <3; i ++){
 if(numbers[i] % 2 === 0){
  result += (result === '' ? '' :', ') + Math.pow(numbers[i], 2)
  count ++;
 }
}
```

- count, result, i 등 실행 중 값이 바뀔 수 있는 변수
- 소프트웨어가 커지고 복잡해 질 수록 이러한 변수들은 위험한 요소
- 특히 여러 스레드가 돌아가는 멀티 스레드 환경에서는 여러 스레드가 한 변수에 접근 할 때 이를 제대로 처리하지 않으면 디버깅도 하기 힘든 상황이 생길 수 있음

```
const numbers = [
 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
]
console.log(
 numbers
  .filter(n => n % === 0)
  .slice(0, 3)
  .map(n => Math.pow(n, 2))
  .join(', ');
)
```

- 함수형 프로그래밍에서는 가능한 변수들을 쓰지 않음
- 순수함수들을 이용하여 외부의 데이터를 변경하지 않음
- 값들을 내부에서 처리해서 밖으로 반환하는 함수, 또는 이런 함수들의 연쇄작용을 사용
- 함수형 프로그래밍은 선언형 프로그래밍의 특징도 가짐
