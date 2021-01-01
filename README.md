# 코코아클론

### display

- inline: in-the-same-line 옆에 또 올 수 있음
- block: 옆에 아무것도 올 수 없다

- inline -> width, height 가 없음

- block -> width, height 가 있음
- box의 특성
  - margin
  - border
  - padding

### margin

```css
- margin: 20px 15px; // 상하 좌우
- margin: 20px 5px 12px 9px; // 위 오른쪽 아래 왼쪽 - 시계방향
```

### viewpoint

- 100vh: 화면 100%

### flexbox

```css
- display: flex
- justify-content: main-axis
- align-items: cross-axis
- flex-direction: row, column // 기준선을 바꿀 수 있음
- flex-wrap: wrap // nowrap: 무조건 한줄, wrap: 크기에 따라 여러줄 가능
```

### Position

- relative: 원래 위치 기준에서 변경
- absolute: relative 된 가장 가까운 부모를 찾는거이다. 아무것도 없으면 최상위 부모인 바디로 적용이 된다. relative를 기준으로 left, right, bottom을 설정하는 것이다.
- static: 기본값
- fixed: 화면 움직여도 고정값 (네비게이션 바 같은거)

### Pseduo selector

```css
div:first-child {
  background-color: tomato; // div의 첫번째 자식을 selector
}
```

```css
div:last-child {
  background-color: teal; // div의 마지막 자식을 selector
}
```

```css
span:nth-child(2),
span:nth-child(4),
span:nth-child(6) {
  background-color: teal;
}
```

```css
span:nth-child(even) {
  background-color: teal;
}
span:nth-child(odd) {
  background-color: tomato;
}
```

```css
span:nth-child(3n + 1) {
  background-color: teal; // 이런식으로 수열로도 가능 (0, 4, 7 ...)
}
```

```css
div span {
  text-decoration: underline; // <div><p><span> 에도 적용이 된다,
}

div > span {
  text-decoration: underline;  <div><span> 에만 적용이 된다. div 바로 자식의 span
}

p + span {
  text-decoration: none; // <p> 바로 다음에 오는 <span>
}

p ~ span {
  color: red; // <p> 다음에 오는 형제<span>
}


```

```css
input:required {
  border: 1px solid tomato;
}
```

```html
<input type="password" required placeholder="password" / >
```

```css
> input:optional {
> border: 1px solid teal;
> }
```

```html
<input type="text" placeholder="username" /
```

```css
input[type="password"] {
  background-color: thistle;
}

input[placeholder="username"] {
  background-color: thistle;
}

input[placeholder~="name"] {
  background-color: thistle; // name 포함
}
```

### State

```css
button:active {
  background-color: tomato;
}

button:hover {
  background-color: teal;
}

input:focus {
  background-color: yellowgreen; /** 키보드 + focus*/
}

a:visited {
  color: teal; /** 방문했을때 색상이 변경*/
}

a:hover {
  color: tomato; /** 방문했을때 색상이 변경*/
}

a:focus {
  color: yellow; /** 방문했을때 색상이 변경*/
}

form:focus-within {
  border-color: seagreen;
  padding: 40px;
}

form:hover input:focus {
  background-color: sienna;
}
```

### Media Query

오직 CSS만을 이용해서 스크린의 사이즈를 알 수 있는 방법.

```css
@media screen and (max-width: 600px) {
  div {
    background-color: tomato;
  }
}

/** 스크린이 width 600 ~ 1200px */
@media screen and (min-width: 601px) and (max-width: 1200px) {
  div {
    background-color: wheat;
  }
}

@media screen and (min-width: 1200px) {
  div {
    background-color: turquoise;
  }
}
```
