# 프론트엔드 JS 관련 면접 질문 모음
## 목차
1. [스코프 (Scope)](#스코프-scope)
1. [호이스팅 (Hoisting)](#호이스팅-hoisting)
1. [var, let, const의 차이](#var-let-const의-차이)
1. [콜백함수 (Callback Function)](#콜백함수-callback-function) 

## 스코프 (Scope)
  * 함수스코프와 블록스코프가 있다
  * 함수스코프는 함수 범위의 스코프를 의미한다.
  * 블록스코프는 블록 단위의 스코프를 의미한다.(if for 같은 명령문 내의 블록에서도 스코프 영향이 있음)
  
## 호이스팅 (Hoisting)
  * 자바스크립트의 변수, 함수 선언을 가장 먼저 읽어 들이는 것
  * 호이스팅은 스코프 단위로 일어난다.

## var, let, const의 차이
  * var는 변수 선언시 변수명이 중복이 허용 됨
  * var는 선언만 해도 undefined를 초기값으로 할당해서 변수 사용이 가능함
    let, const는 직접 할당하지 않으면 TDZ(Temporal Dead Zone) 상태가 되어서 에러가 발생
  * var는 함수 스코프, let, const는 블록스코프

## 콜백함수 (Callback function)
 * 함수의 파라미터로 들어가는 함수(함수를 실행하는 함수)
 * 상태변화, 액션의 변화 등에 실행하고 싶은 것
 * 특정 코드를 순차적 실행을 하기 위함
 ~~~ javascirpt
  //콜백은 대략 이런 구조를 가지고 있다고 볼 수 있다.
  
  function doSometing(param){
    console.log(start);
    param();
  }
  
  function callback(){
    console.log(callback);
  }
  
  doSometing(callback)
 ~~~
 * 서버통신을 할때 통신 성공, 실패 여부를 기본적으로 콜백으로 요청해야하는데, 이런 통신처리가 2~3번만 중첩되도 코드의 순서 파악이 어려워짐
 
 ~~~ javascirpt
  //만약 회원 api에서 id를 취득하고 결제 api에서 amount를 취득한뒤에 vip 회원 인지 판단하는 과정을 콜백으로만 구성해보면
  
  function doSometing(param){
    console.log(start);
    param();
  }
  
  function callback(){
    console.log(callback);
  }
  
  doSometing(callback)
 ~~~
## Promise
 * 비동기 처리에 사용되는 객체
 * 콜백 중첩을 막기 위해서 고안
 
 *** javascirpt
 
 ***
 
## async await
