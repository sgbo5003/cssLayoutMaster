# cssLayoutMaster
노마드코더 - CSS Layout 마스터클래스 강의

## #1 FLEXBOX
-------------
### #1.1 First Rule of Flexbox

> flexbox
> 
- 항상 붙어있는 부모가 자식의 위치를 움직일 수 있다.
- flexbox에서 box들의 위치를 바꾸고 싶으면 flex container의 안에 있어야 한다.
- flex container를 만드는 법
    - `display: flex`


### #1.2 Main Axis and Cross Axis

> Main Axis & Cross Axis
> 
- Main Axis
    - = justify-content
- Cross Axis
    - = align-items

### #1.3 Column and Row

> flex-direction: row 일 때
> 
- main axis : 가로
- cross axis : 세로
- justify-content : 가로축에 영향
- align-items: 세로축에 영향

> flex-direction: column 일 때
> 
- main axis : 세로
- cross axis : 가로
- justify-content : 세로축에 영향
- align-items: 가로축에 영향

### #1.4 align-self and order

> align-self
> 
- align-items와 비슷하다.
- 각각의 item을 제어 가능

> order
> 
- default 값 0
- order의 값이 낮을수록 앞에 위치하게 된다.

### #1.5 wrap, nowrap, reverse, align-content

> flex-wrap
> 
- 줄바꿈에 관한 것들

> reverse
> 
- reverse에 관한 것들

> align-content
> 
- 선을 변경한다.
- cross-axis 에서 변경
- 줄 사이 공간을 변경

### #1.6 flex-grow, flex-shrink

> flex-shrink
> 
- flexbox가 쥐어짜질때 얼마나 줄어들지를 정함
- 기본값 1

> flex-grow
> 
- flex-shrink와 반대로 얼마나 증가할지를 정함
- 기본값 0

### #1.7 flex-basis

> flex-basis
> 
- flex-shrink 와 flex-grow 를 위한 기본 세팅
- main axis(주축) 쪽 크기를 정해준다

### #1.8 Flexbox Froggy 1-13 ~ #1.9 Flexbox Froggy 14-24

> flexboxfroggy 게임을 통한 실습
> 
- [https://flexboxfroggy.com/#ko](https://flexboxfroggy.com/#ko)

### #2.1 Life Before Grid

> Grid를 사용하는 이유
> 
- flex로 grid 형태를 구현하기가 어려워서

### #2.2 CSS Grid Basic Concepts

> 그리드를 시작
> 
- `dispaly: grid;`

> grid-template-columns, grid-template-rows
> 
- gird-template-columns
    - 행의 크기 조정 기능
- gird-template-rows
    - 열의 크기 조정 기능

> gap
> 
- 행 과 열 사이의 간격을 설정

### #2.3 Grid Template Areas

> repeat()
> 
- `repeat(개수, 크기)`

> grid-template-areas & grid-area
> 

```jsx
.grid {
  display: grid;
  grid-template-columns: repeat(4, 200px);
  grid-template-rows: 100px repeat(2, 200px) 100px;
  grid-template-areas: 
  "header header header header"
  "content content content nav"
  "content content content nav"
  "footer footer footer footer";
}

.header {
  background-color: #2ecc71;
  grid-area: header;
}
.content {
  background-color: #3498db;
  grid-area: content;
}
.nav {
  background-color: #8e44ad;
  grid-area: nav;
}
.footer {
  background-color: #f39c12;
  grid-area: footer;
}
```

- grid-area에 있는 이름과 grid-template-areas에 있는 이름이 같아야 한다.

> grid가 적용되지 않을 때
> 
- grid 내부에 grid-area의 영역이 전부 이어져 있는가? (ex: header 영역이 둘로 쪼개져 있고 그러면 안됨.)
- grid 내부에 grid-area의 영역이 직사각형인가? (ex: header 영역이 ㄴ자 ㄱ자 등이어도 안됨.)

### #2.4 Rows and Columns

> `grid-column-start` `grid-column-end` `grid-row-start` `grid-row-end`
> 
- 자식 grid에 명시한다.
- 행과 열의 크기 설정 가능
- 사용 예시
    
    ```jsx
    .header {
      background-color: #2ecc71;
      grid-column-start: 1; // 첫번째 라인부터
      grid-column-end: 5; // 5번째 라인까지
    }
    ```

### #2.5 Shortcuts

> 줄여쓰기
> 

```css
/* 예시 5개의 라인이라고 가정 했을 시 */
.header {
	grid-column-start: 1;
	grid-column-end: 5;
}

/* 줄여쓰기 1 */
.header {
	grid-column: 1 / 5;
}

/* 줄여쓰기 2 */
.header {
	grid-column: 1 / -1; /* 끝에서부터 라인을 셀때는 -1, -2, -3..으로 센다.*/
}

/* 줄여쓰기 4 */
.header {
	grid-column: span 4; /* (start) / span (cell 수) */
}

```

### #2.7 Grid Template

> fraction
> 
- grid에서 사용가능한 공간을 뜻한다.
- 표기법 : `1fr`
- gird container의 width, height가 정해져 있지 않다면 기본 width는 화면 전체너비 이고, height는 0이다.

> grid-template
> 

```css
.grid {
  display: grid;
  gap: 10px;
  height: 50vh;
  grid-template: 
  "header header header header" 1fr
  "content content content nav" 2fr
  "footer footer footer footer" 1fr
  ;
}
```

### #2.8 Place Items

> 정렬, 배치
> 
- `justify-items`
- `align-items`
- `place-items: (수직) (수평);`
    - place-items : align-items / justify-content 순서
