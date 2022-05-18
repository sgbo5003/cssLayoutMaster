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
