# 매칭해 주개
>
> 아카데미 1차 프로젝트
>
<img width="436" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/7443eefb-b871-439f-94ed-09690d6f1691">

* 프로젝트 기간: 2023.10.13 ~ 2023.11.15
<br/>

## 사용 툴 구성
_BACKEND_
<br/>
<img src="https://img.shields.io/badge/JAVA-007396?style=for-the-badge&logo=java&logoColor=white"> 
<img src="https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
<img src="https://img.shields.io/badge/mybatis-007396?style=for-the-badge&logo=mybatis&logoColor=white">
<img src="https://img.shields.io/badge/mariaDB-003545?style=for-the-badge&logo=mariaDB&logoColor=white">

<br/>
<br/>

_FRONTEND_
<br/>
  <img src="https://img.shields.io/badge/CSS-7952B3?style=for-the-badge&logo=css3&logoColor=white"> 
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 
  <img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white">
<br/>
<br/>

_기타_
<br/>
<img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">


<br/><br/>

## 프로젝트 설명

'**매칭해주개**'입니다.

> 강아지 산책 메이트 매칭 프로그램<br/>
> 여러 마리 강아지 프로필을 등록할 수 있습니다.<br/>
> 대표 프로필로 등록된 강아지와 잘 맞는 강아지 리스트를 받아 마음에 드는 강아지에게 매칭 요청을 보낼 수 있습니다.<br/>
> 채팅을 통해 약속을 잡을 수 있습니다.<br/>
> 회원 등급에 따라 볼 수 있는 리스트 수와 보낼 수 있는 채팅 수가 제한됩니다.<br/>

<br/>

## 개발자

* [김인혜](https://github.com/kimIHNiCole) - 개인 정보/강아지 프로필 관리 + 등급/권한 관리
* [김세연](https://github.com/SEYEON94) - 채팅 + 매칭 요청 전반
* [이한준](https://github.com/leehj1083) - 로그인 / 회원가입 + 회원 관리
* [전은호](https://github.com/eh09) - 커뮤니티
* [정지원](https://github.com/jungjiwon970) - 강아지 프로필 등록 + 신고 관리
* [차재호](https://github.com/ckwogh) - 랜덤 매칭 리스트 + 데이터 수집
<br/><br/>

## 핵심 기능
<img width="900" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/62e1db3c-c568-4fce-a886-780cc5678d20">
<br><br/>

### 매칭 리스트
> 입력된 동 주소가 일치하는 리스트를 추출합니다.<br><br/>
> 해당 리스트 중 등록된 강아지들의 성향이 내 강아지의 성향과 네 가지 > 세 가지 > 두 가지 > 한 가지 일치하는 순서대로 리스트를 가져오되, ORDER BY RAND() 함수를 사용하여 해당 리스트 중 필요한 수만큼의 랜덤값을 가져옵니다.
<br><br/>
> 매칭 요청을 할 경우 해당 user 의 아이디, 대표 프로필로 등록한 강아지의 profile 아이디 값을 가져와 매칭 요청을 받은 견주 user 의 아이디의 리스트에 받은 강아지의 profile 아이디와 함께 출력합니다.  
<br><br/>

<img width="900" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/1bac0ba9-a508-43c1-a728-28f3b84dde9a">

### 채팅 서비스

> 1:1 채팅을 효율적으로 구현하기 위해 롱 폴링(Long Polling) 방식을 이용한 채팅 서비스를 합니다.<br><br/>
> session 에 저장된 user 아이디와 매칭 요청 받은 리스트에 저장된 강아지의 profile 아이디로 채팅방을 생성하며, session 체크를 통해 본인만 접근이 가능하도록 하였습니다.<br><br/>


<img width="900" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/49128731-1f80-4cd3-b88a-cbf8a65ed6dd">

### 매너견 평가
> DB에 Default Value를 설정하여 평가를 받을 때마다 +1 / -1 을 처리해 줍니다.<br><br/>
> 일정 이상의 점수일 때 매너견으로 표시되며 일정 이하의 점수일 때 비매너견으로 표시됩니다.<br><br/>


<br><br/>

## 구현 화면

<br><br/>

### 회원 가입 페이지
<img width="472" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/a4bfd08e-80e8-4c26-ad44-db334a2c66ba">
<img width="516" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/e54542fe-9ab0-4297-8436-d630145aa6e7">
<img width="445" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/a3aa869e-21d1-4d6e-a79f-e93eb89c0de9">

<br><br/>

### 메인 페이지
<img width="800" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/f4d975ff-1c76-443d-a420-1278590592e9">
<img width="674" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/46ff3514-f599-4dfa-8dcd-5c624bc7cb7d">

<img width="500" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/3146c3d7-d952-4b16-9c65-d1d50967e6e8">


<br><br/>

### 받은 매칭 리스트 페이지
<img width="961" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/b9850b21-fcd2-48b1-b35c-98b785771c34">

<br><br/>


### 채팅 페이지
<img width="953" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/cf0c2fb1-f325-4e1d-a12c-46498d4bf9f9">
<img width="346" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/0ccf0ee8-2252-40c7-bb48-b184b53047aa">


<br><br/>

### 프로필 페이지
<img width="492" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/fa0dca07-e50f-43b0-98d3-f34797cd6aac">

<br><br/>

### 관리자 페이지
<img width="957" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/c77a2292-5700-4067-a0f0-6b9e3a06f44f">

<br><br/>


## DB ERD

<img width="1062" alt="image" src="https://github.com/kimIHNiCole/MatchDog/assets/142763051/eeaae18d-354e-403b-abbf-00477f16cd43">




```



