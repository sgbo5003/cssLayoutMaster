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