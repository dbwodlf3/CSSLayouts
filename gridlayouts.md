# Grid Layout

Grid Layout은 미리 가상의 선을 긋고, 그 가상의 선에 알맞게끔 배치하는 Layout을 말합니다.
컨테이너가 존재하며 이 컨테이너의 프로퍼티 값은 display:grid 가 됩니다.
가상의 선을 긋는 방법은 컨테이너에서 행해집니다.

[여기](https://css-tricks.com/snippets/css/complete-guide-grid/)에서 자세히 정리된 CSS GRID Layout에 대한 정리를 볼 수 있습니다.

가상의 선을 긋는 것은 grid-template-columns 속성과 grid-template-rows 속성을 이용합니다.
### 선 나누기
```css
grid-template-columns: 40px 50px auto 50px 40px;
grid-template-row: 25% 100px auto;
```

나뉘어진 영역을 한덩어리로 묶는 방법으로는 grid-template-ares 라는 속성이 있습니다.
공간이 나뉘어지면, 해당 공간에 이름을 붙여서 할당합니다. 이 때에 "." 은 빈공간을 나타냅니다.

### 공간 나누기

```css
.item-a {
  grid-area: header;
}
.item-b {
  grid-area: main;
}
.item-c {
  grid-area: sidebar;
}
.item-d {
  grid-area: footer;
}

.container {
  display: grid;
  grid-template-columns: 50px 50px 50px 50px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
```

![https://css-tricks.com/snippets/css/complete-guide-grid/](./dddgrid-template-areas.svg)

### element property

그리드 레이아웃의 차일드에게는 몇가지 속성값이 있습니다.
grid-column-strat&end
grid-row-start&end
grid-area
의 경우에는 그리드 레이아웃에서 어느 영역을 차지할 것인지를.

justify-self
aligin-self
place-self
같은 경우에는 해당 영역내에서 정렬(align)을 어떻게 할 것인지에 대한 속성입니다.