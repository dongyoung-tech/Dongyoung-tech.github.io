---
title:  "자바스크립트 export&imports" 
excerpt: 자바스크립트 export&imports" 
categories:
  - Javascript
tags:
  - [javascript]

toc: true
toc_sticky: true
 
date: 2023-01-25
last_modified_at: 2023-01-25

---

<h2>자바스크립트의 exports&import</h2>
<p>최신 자바스크립트 에서는 모듈방식으로 코드를 작성할수 있는 기능이 있어서 , 코드를 여러개로 분할한 후, html에 차례대로 불러올수 있다 </p>


```
//person.js

const person ={
  name : 'Lee'
}
export default person
```
이렇게 파일을 작성하면 다음과 같이 import 할 수 있다

```
//index.js
import person from './person.js'
```
이 때는 꼭 person 이 아니라 다른 이름을 사용해도 된다.

하지만, 

```
//person.js

export const name = 'Lee';
export const SayHello() ={....}
```
이런식으로 export 하면,

이름을 지정해서 import 해주어야 한다.

```
//index.js
import {name} from './person.js'
import {SayHello} from './person.js'
```