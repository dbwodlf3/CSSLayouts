## flexbox-container

display:flex.
보통 felxbox 라고 부르는 이것은 inner display type을 설정하는 css 속성값입니다.
flex container안의 아이템들에 대한 flow layout을 정의합니다.

flex-direction과 flex-wrap을 묶은 flex-flow 라는 shorthand property가 존재합니다.

flex-direction은 내부의 item 들의 flow 방향을, flex-wrap은 컨테이너 내부에서 확장되는 item 들을 어떻게 할 것인지 결정합니다. wrap은 flow를 따라서 container도 확장되는 반면, nowrap 에서는 flow를 따라서 container의 크기가 확장 되지 않습니다. item 들은 그저 overflow 될 뿐입니다.

justify-content와 align-items라는 속성이 있습니다.
justify-content는 아이템들의 위치를 결정합니다. 가로(수직선분)를 기준으로 아이템들을 정리합니다.
align-items는 아이템들의 위치를 결정합니다. 세로(수평선분)를 기준으로 아이템들을 정리합니다.

align-contents라는 속성이 있습니다.
이것은 flex line을 설정합니다...

아래의 사진은 align-content의 examples 입니다.
![https://css-tricks.com/almanac/properties/a/align-content/](./align-content-example.svg)

## flexbox-items

Flexbox가 적용된 컨테이너속의 item들은 flex의 값들을 적용받을 수 있습니다.
flex-grow, flex-shrink, flex-basis 세가지 속성에 대한 flex 라는 shorthand property가 존재합니다.
그 외에는 order, align-self 속성이 존재합니다.

### 개념정리

박스내의 flow를 임의로 설정한다는 것에 의의가 있습니다.
이전에는 flow를 바꾸기 위해서 이것저것 작은 값들을 손대어야 했지만, flex box 를 이용하면 flex의 속성값들만을 바꾸어서 임의의 flow를 쉽게 만들어낼 수 있습니다.