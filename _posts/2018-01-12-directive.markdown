---
layout: post
title:  "Directives!"
date: 2018-01-12 12:08:00 +0900
categories: Vue
---

#Directives

레퍼런스에서는,
> 디렉티브는 `v-` 접두사가 있는 특수 속성입니다. 디렉티브 속성 값은 단일     **JavaScript 표현식** 이 됩니다. (나중에 설명할 `v-for`는 예외입니다.) 디렉티브의 역할은 표현식의 값이 변경될 때 사이드이펙트를 반응적으로 DOM에      적용하는 것 입니다.
, 라고 함

Directives, 메소드 느낌.
Vue 엘리먼트에서 사용되는 특별한 속성
기능상에 있어서 중요한 역할을 함

| Directives | 설명 |
| ------ | ------ |
| `v-text` | text 값 출력 |  
| `v-html` | html 태그 읽음 |  
| `v-show` | visible:true/false 값에 따른 출력 |  
| `v-if` `v-else` `v-else-if`| 경우의 실행 |
| `v-pre` | 지시문을 무시함 {{}}을 그대로 출력 |
| `v-cloak` | 준비되기 전 까지 HTML 코드를 숨김 |
| `v-once` | 한번 렌더링(ex. value 값이 변해도 초기값에 고정) |  

##전달인자

`v-bind`
HTML 엘리멘트 속성에 데이터 값 삽입을 원할 때,
Mustach({{}})는 에러가 날 껄~
```
<a href="{{url}}"> ... </a>          에러
```
이 때, `v-bind`가 필요함
>Use v-bind or the colon shorthand instead.
친절하게 콘솔창에서 알려줌 :)

엘리먼트의 href 속성을 표현식 url의 값에 바인드하는 v-bind 디렉티브에게 알려줌
```
<a v-bind:href="url"> ... </a>
<a :href="url"> ... </a>             약어
```

`v-on`
DOM 이벤트를 수신
```
<a v-on:click="doWhat"> ... </a>
<a @click="doWhat"> ... </a>         약어
```
자바스크립트 onclick 과 동일한 액션

---
