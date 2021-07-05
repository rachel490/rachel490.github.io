---
title: '[TIL] D1'
date: 2021-07-05 23:47:50
category: 'TIL'
draft: false
---

- [x]  카카오클론 챌린지 day1
- [x]  바닐라 JS #3.6 - #4.3

- Login Validation Check를 사용하려는 경우 div가 아닌 form으로 input을 감싸줘야함.
- classList : class를 배열로써 접근하는 방식

    → classList.add = class를 추가시킴

    → classList.remove = class를 제거시킴

- 많은 이벤트들은 기본적인 default action이 존재

    ⇒ submit을 하면 default로 새로고침을 함, a태그의 경우 click하면 link로 넘어감 등..

    ⇒ default action을 막기 위해서 event.preventDefault() 사용

- event 객체의 경우 eventHandling 함수에서 기본적으로 들어있는 정보.

    ⇒ 해당 event에 대한 정보들이 담겨져있는 객체. preventDefault는 메소드 중 하나.