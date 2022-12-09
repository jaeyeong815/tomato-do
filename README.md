
# Tomato-do (뽀모도로 타이머 + 투두리스트)

[1. 프로젝트 간단 설명](#description) <br>
[2. 개발자 소개](#developers) <br>
[3. 프로젝트 소개](#about-project) <br>
[4. 내가 기여한 부분](#내가-기여한-부분) <br>
[5. 트러블 슈팅]() <br>
[6. 구현 화면](#results)

---

## Description
> 2022.04. - 2022.05. (1개월) <br>
> [오늘도 Tomato-do! (서비스 링크)](https://happy-jm.github.io/Tomato-do/) <br/>
> [Team Notion](https://www.notion.so/tomato-do/Tomato-do-37daf0329b314e6c81ae99cb37fa2899)

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
	
<br>

## 내가 기여한 부분

### 1. 주제 의견 제시

투두리스트 + 뽀모도로 타이머 주제 제안, 의견 채택 <br>
[프로젝트 이름 및 레이아웃 의견 제안 Notion](https://tomato-do.notion.site/f8e9abc927294d51adc99987e0bcea13)

### 2. 타이머 기능 개발

JS내장 매서드인 `setInterval()` `clearInterval()` 사용하여 기능 구현

![image](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a8fe06ce-257a-44b2-9cf8-13b9767c540c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-11-25_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_2.18.53.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221209%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221209T030900Z&X-Amz-Expires=86400&X-Amz-Signature=fddffd0ac83a006946942f86127e4c966ca974d9637eeaa6451b2ee2c371fa29&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA%25202022-11-25%2520%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE%25202.18.53.png%22&x-id=GetObject)

### 3. UX 개선사항 의견 제시 및 개선

**1. 예외 처리**

- 할 일을 미입력하고 등록 버튼 클릭 시 사용자에게 안내되도록 alert 제안 ➡️ ‘할 일을 입력해주세요!’ 안내 <br>

	<img width="1267" alt="스크린샷 2022-12-09 오후 12 19 38" src="https://user-images.githubusercontent.com/85178602/206616829-cda2ebbe-a140-4c55-8da5-972e6e6d4cdd.png">
- 할 일 삭제 시 한 번 더 확인을 위해 삭제 안내 alert 제안 ➡️ ‘정말 삭제하시나요?’ 안내 <br>

	<img width="1268" alt="스크린샷 2022-12-09 오후 12 19 56" src="https://user-images.githubusercontent.com/85178602/206616822-48708b56-4eca-4982-9b31-232cc2c36860.png">
	
**2. 뱃지 기능 수정**

- 안내 문구 수정 및 상황 별 로직 수정 [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/3fa0b7acc3c7cc3ac9236ee63f7da8ea0065b02a) <br>

	https://github.com/jaeyeong815/tomato-do/blob/d98a6a961734b46dfa1a3508882801d331e0c0a0/badge.js#L21-L77

**3. 웰컴 페이지 개선**

- 배경색상 변경 및 이미지 추가, 문구 변경 [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/3fa0b7acc3c7cc3ac9236ee63f7da8ea0065b02a) <br>

	https://github.com/jaeyeong815/tomato-do/blob/d98a6a961734b46dfa1a3508882801d331e0c0a0/index.html#L247-L256

- 디자인 개선 [커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/c14a8fb699613073305eb50868413f90b33f9d13) <br>

	https://github.com/jaeyeong815/tomato-do/blob/3fa0b7acc3c7cc3ac9236ee63f7da8ea0065b02a/tomato-do.css#L779-L786

**4. 파비콘 설정**

[커밋 링크](https://github.com/jaeyeong815/tomato-do/commit/52f7d73fed155beee1011ab018015ce194a7f424) <br>

https://github.com/jaeyeong815/tomato-do/blob/d98a6a961734b46dfa1a3508882801d331e0c0a0/index.html#L18-L23

<br>

## 트러블 슈팅

<br>

## Results
### Web

|기능|화면|
|:---:|:---:|
|투두리스트 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|<img src="./img/todolist.png"  width="30%"/>|
|타이머|<img src="./img/timer.png"  width="30%"/>|
|다크모드|<img src="./img/nightmode.png"  width="50%"/>|

---
<br>

<div align=center>

![image](https://user-images.githubusercontent.com/102483942/169540397-71d32a84-e6df-412e-848e-7f9a27689908.png)
![image](https://user-images.githubusercontent.com/102483942/169540482-2d8d8310-f1b5-4afe-bca2-23c82e66dc97.png)
![image](https://user-images.githubusercontent.com/102483942/169540641-5148effa-6bbe-4c2e-8d8f-705e9ebef874.png)
![image](https://user-images.githubusercontent.com/102483942/169540896-da8d0e30-e08c-4f94-bd61-37816cba4519.png)

</div>
