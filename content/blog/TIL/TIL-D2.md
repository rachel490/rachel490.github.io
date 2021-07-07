---
title: '[TIL] D2'
date: 2021-07-07 23:42:50
category: 'TIL'
draft: false
---

- [x]  카카오클론 챌린지 day3
- [x]  바닐라 JS 완강 

- localStorage 이용해서 db 저장 
    - localStorage.set('key',value)
    - localStorage.get('key')
    - localStorage에 저장할 때는 string 형태로만 저장가능 -> JSON.stringify 사용해서 변환
    - localStorage에서 가져올 때 원래 형태로 변환 필요 -> JSON.parse 사용
- forEach, filter : iterate이 가능한 배열에 쓰임. 콜백함수를 인자로 갖음. 콜백함수를 호출할때 배열의 원소 하나하나를 넣어서 호출함. 자동적으로 매개변수만 넣어주면 item 객체를 사용할 수 있음.