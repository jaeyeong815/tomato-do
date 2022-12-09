
# Tomato-do
뽀모도로 타이머 + 투두리스트

[1. 🗒️ 프로젝트 간단 설명](#description) <br>
[2. 👩🏻‍💻 개발자 소개](#developers) <br>
[3. 🌎 프로젝트 소개](#about-project) <br>
[4. 💁‍♀️ 내가 기여한 부분](#내가-기여한-부분) <br>
[5. 🔫 트러블 슈팅](#트러블-슈팅) <br>
[6. 🖥️ 구현 화면](#results)

---

## Description
> 2022.04. - 2022.05. (1개월) <br>
> [오늘도 Tomato-do! (서비스 링크)](https://happy-jm.github.io/Tomato-do/) <br/>
> [Team Notion](https://tomato-do.notion.site/tomato-do/Tomato-do-37daf0329b314e6c81ae99cb37fa2899)

### Summary

* 투두리스트, 타이머, 프로필, 뱃지, 테마 기능
* IndexedDB 사용으로 인한 브라우저(기기) 변경 시 데이터 이동 불가능

<br>

## Developers
<img src="https://avatars.githubusercontent.com/u/102483942?v=4" width="80" height="80">|<img src="https://avatars.githubusercontent.com/u/98958768?v=4" width="80" height="80">|<img src="https://avatars.githubusercontent.com/u/94153997?v=4" width="80" height="80">|<img src="https://avatars.githubusercontent.com/u/59535609?v=4" width="80" height="80">|<img src="https://avatars.githubusercontent.com/u/85178602?v=4" width="80" height="80">|<img src="https://avatars.githubusercontent.com/u/82685793?v=4" width="80" height="80">|
|:---:|:---:|:---:|:---:|:---:|:---:|
|[FE 서정민](https://github.com/HAPPY-JM)|[FE 김동철](https://github.com/GreyFBTT)|[FE 지재영](https://github.com/jaeyeong815)|[BE 배성현](https://github.com/seonghbae)|[BE 박태훈](https://github.com/ekdh0858)|[BE 이수정](https://github.com/tinashome)|

<br>

## About Project

### FE

<img src="https://img.shields.io/badge/Language-HTML-green?style=flat"/> <img src="https://img.shields.io/badge/Language-CSS-green?style=flat"/> <img src="https://img.shields.io/badge/Language-JavaScript-green?style=flat"/>

* 투두리스트 : DB와 통신하여 CRUD 기능 수행
* 타이머 : 집중-휴식 타이머 기능, 집중 타이머 종료시 음성알람 제공, 타이머 사용 시 시간 정보 DB에 저장
* 프로필 : 이름, 사진
* 뱃지 : DB에 쌓인 시간 데이터에 따른 뱃지 제공
* 테마 : 데이-나이트 모드

### BE

<img src="https://img.shields.io/badge/Language-JavaScript-green?style=flat"/> <img src="https://img.shields.io/badge/DB-IndexedDB-yellow?style=flat"/>

* IndexedDB 사용
* IndexedDB 구조
	```js
	todolist:  "++id,todo,check",
	time:  "++id",
	userInfo:  "++id,userName,userimg,type",
	report:"++id,date,startTime,endTime"
	```
	
[⬆️ TOP](#tomato-do)

<br>

## 내가 기여한 부분

### 1. 주제 의견 제시

투두리스트 + 뽀모도로 타이머 주제 제안, 의견 채택 <br>
[프로젝트 이름 및 레이아웃 의견 제안 Notion](https://tomato-do.notion.site/f8e9abc927294d51adc99987e0bcea13)

### 2. 타이머 기능 개발

JS내장 매서드인 `setInterval()` `clearInterval()` 사용하여 기능 구현

<img alt="스크린샷 2022-11-25 오후 2 18 53" src="https://user-images.githubusercontent.com/85178602/206625090-f48562ec-f522-417b-b768-5a9ecb0d3985.png" width="70%">


### 3. UX 개선사항 의견 제시 및 개선

**1) 예외 처리**

- 할 일을 미입력하고 등록 버튼 클릭 시 사용자에게 안내되도록 alert 제안 ➡️ ‘할 일을 입력해주세요!’ 안내 <br>

	<img width="60%" alt="스크린샷 2022-12-09 오후 12 19 38" src="https://user-images.githubusercontent.com/85178602/206616829-cda2ebbe-a140-4c55-8da5-972e6e6d4cdd.png">
- 할 일 삭제 시 한 번 더 확인을 위해 삭제 안내 alert 제안 ➡️ ‘정말 삭제하시나요?’ 안내 <br>

	<img width="60%" alt="스크린샷 2022-12-09 오후 12 19 56" src="https://user-images.githubusercontent.com/85178602/206616822-48708b56-4eca-4982-9b31-232cc2c36860.png">
	
**2) 뱃지 기능 수정**

- 안내 문구 수정 및 상황 별 로직 수정 [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/3fa0b7acc3c7cc3ac9236ee63f7da8ea0065b02a) <br>

	https://github.com/jaeyeong815/tomato-do/blob/d98a6a961734b46dfa1a3508882801d331e0c0a0/badge.js#L21-L77

**3) 웰컴 페이지 개선**

- 배경색상 변경 및 이미지 추가, 문구 변경 [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/3fa0b7acc3c7cc3ac9236ee63f7da8ea0065b02a) <br>

	https://github.com/jaeyeong815/tomato-do/blob/d98a6a961734b46dfa1a3508882801d331e0c0a0/index.html#L247-L256

- 디자인 개선 [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/c14a8fb699613073305eb50868413f90b33f9d13) <br>

	https://github.com/jaeyeong815/tomato-do/blob/3fa0b7acc3c7cc3ac9236ee63f7da8ea0065b02a/tomato-do.css#L779-L786

**4) 파비콘 설정**

- [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/52f7d73fed155beee1011ab018015ce194a7f424) <br>

	https://github.com/jaeyeong815/tomato-do/blob/d98a6a961734b46dfa1a3508882801d331e0c0a0/index.html#L18-L23

[⬆️ TOP](#tomato-do)

<br>

## 트러블 슈팅

### 문제점

> **어떤 상황에서도 집중 시간이 25분으로 재시작되는 문제**
1. 처음 집중시간 50분을 클릭하여 실행하면 정상 작동 된다.<br>
   이후 리셋버튼을 클릭하면 집중 시간이 50분으로 다시 설정되어야 하는데,<br>
   기본값인 25분으로 설정 된다.
    
2. 리셋버튼을 클릭하지 않고 집중시간에서 휴식시간까지 도달하면<br>
   자동으로 처음 실행했던 집중시간이 재시작된다.<br>
   하지만 50분이 아닌 25분으로 재시작된다.<br>

### 원인

> **resetTimer함수에 하드코딩 되어있는 타이머 정보**

<details>
<summary>1번 문제점의 원인</summary>
<div markdown="1">
<br>
1. 사용자의 버튼 클릭 이벤트를 추적하고, 선택한 시간 값을 알기 위해 timerTimeSet 함수를 생성<br>
2. 사용자가 처음 50분 - 10분 버튼을 클릭하면 timerTimeSet함수에 의해 변수값이 제대로 할당되어 정상 작동<br>
3. 리셋버튼 클릭 시 실행되는 resetTimer함수에 기본값이 25분 - 5분으로 작성되어있어 리셋버튼을 클릭하면 무조건 25분으로 설정 됨<br>
</div>
</details>

<details>
<summary>2번 문제점의 원인</summary>
<div markdown="1">
<br>
1. 뽀모도로 타이머는 집중타이머가 끝나면 휴식타이머가 바로 작동하는 로직, 이후 휴식타이머가 끝나면 집중타이머가 이어서 재작동<br>
2. 휴식타이머인 restStart함수가 끝나면 resetTimer 함수가 실행된 다음 집중 타이머가 재실행<br>
3. 이 때 1번 문제점의 원인과 동일한 이유인 resetTimer 함수의 기본 설정 값때문에 25분으로 집중 타이머가 실행됨<br>
</div>
</details>

### 해결

> **상태값 변수를 생성하여 변화를 감지 및 설정**

[커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/993bd649a2b2220fcad131c0c8575667faa80511)

현재 타이머의 상태값을 알 수 있도록 하는 `selectOption`변수를 생성하고<br>
`select`함수를 만들어 사용자가 선택 한 시간에 따라 값이 초기화 될 수 있도록 개선했다.<br>

또한 `select`함수에는 `selectOption`값이 바뀌면 시간 설정이 다시 될 수 있도록<br>
`timerTimeSet`함수를 함께 작성해주었다.<br>

https://github.com/jaeyeong815/tomato-do/blob/5d6bc0aa07f6a7d4ae7b89fb8492aa056256cc42/timer.js#L34-L69

[⬆️ TOP](#tomato-do)

<br>

## Results
### Web

|기능|화면|
|:---:|:---:|
|투두리스트 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|<img src="./img/todolist.png" width="30%"/>|
|타이머|<img src="./img/timer.png"  width="30%"/>|
|다크모드|<img src="./img/nightmode.png"  width="50%"/>|

[⬆️ TOP](#tomato-do)

---
<br>

<div align=center>

![image](https://user-images.githubusercontent.com/102483942/169540397-71d32a84-e6df-412e-848e-7f9a27689908.png)
![image](https://user-images.githubusercontent.com/102483942/169540482-2d8d8310-f1b5-4afe-bca2-23c82e66dc97.png)
![image](https://user-images.githubusercontent.com/102483942/169540641-5148effa-6bbe-4c2e-8d8f-705e9ebef874.png)
![image](https://user-images.githubusercontent.com/102483942/169540896-da8d0e30-e08c-4f94-bd61-37816cba4519.png)

</div>

[⬆️ TOP](#tomato-do)
