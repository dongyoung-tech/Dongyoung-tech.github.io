---
title:  "리액트 Export & Import" 
excerpt: "리액트 Export & Import" 
categories:
  - React
tags:
  - [React]

toc: true
toc_sticky: true
 
date: 2023-06-27
last_modified_at: 2023-06-27

---

<h1>리액트 Export & Import</h1>

<h2>What is Export & Import</h2><hr>
<p>
React 로 개발을 하다보면 파일을 나누어서 개발을 하게되는데, 
분리된 파일들을 모듈(module) 이라고 부른다
<br>
다른 모듈안에있는 값을 불러오는것을 import 라고 하고, 모듈내의 값을 외부로 보내는것을 export 라고한다.
</p>

<h2>EXPAMPLE</h2>
<hr>

```
person.js//

const person={
    name:"Lee"
}

export default person
```
```
utility.js///

export const clean =()=>{...}

export const baseData = 10;
```
```
app.js///

import person from './person.js'
import{baseData} from './utility.js'
```

default 키워드 는 다른모듈에서 가져올때 default 로 표시한것을 기본으로 가져온다는 뜻이다.<br>
app.js 에서 person.js 에서 import 하면 default 로 표시한것을 가져온다.(꼭 person 을 사용하지 않고 아무 키워드나 사용해도됨)<br>
utility.js 에서는 default 를 사용하지 않았고 중괄호 (named export) 를 사용하서 import 하였기 때문에 해당 이름이 붙은? 것을 가져온다

```
임포트하는 다양한 방식

import {smth} from './utility.js'
import {smth as Smth} from './utility.js' => smth 라는 변수를 가져와서 Smth 로 사용하겠다 라는 뜻.
import * as bundled from './utility.js' => 모듈내의 모든 내용을 가져와서 bundled 라는 객체로 묶는다는 뜻.
```

