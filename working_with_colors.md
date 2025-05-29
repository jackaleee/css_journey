# Colors in CSS

## Теория
__Цвета делятся на:__ 
- Основные (red, blue, yellow)
- Дополнительные (смесь основных)

Есть цветовые схемы, но про них особо нечего рассказать. Есть такие как Analogous (рядом на круге), Monochromatic (один цвет + его оттенки) и тд. 
<br>
## Named colors
Простыми словами, это те цвета, которые вы прописываете, тх всего 140, это самый простой вариант. Пример: `color: red;`
## rgb & rgba 
'rgba(red, green, blue, opacity (alpha)' Тут все просто, можно задать число от 0 до 255, в альфе от 0 до 1. 
## hsl & hsla
Тут немного сложнее закручено все `hsla(hue, saturation, lightness, alpha)`. Значение Hue задается в градусе цветового круга. К примеру red = 0, макс. значение 360. Saturation уже тдет в процентах (от 0% до 100%) где 0 - это буквально оттенок серого, а 100 - полноценный цвет. Lightness так же в процентах от 0% до 100%, где 50% это цвет без изменений, 100% это белый цвет, а 0% = черный. Так же как и в rgba можно добавить прозрачность через alpha (range from 0 to 1).
## HEX (шеснадцатиричная система)
'#RRGGBB' самый адекватный вариант, так как можно взять цвет с фигмы и просто подставить. FF = 255, 00 = 0. 
## Gradients (Linear, Radial) 
`linear-gradient(direction, color1, color2,...)` из интересного, это можно самому выбирать на каком проценте будет переход градиента в другой цвет вот таким образом `linear-gradient(to right, red 20%, blue 60$)`. По дефолку расстояния идут 0, 50, 100%. Так же по дефолту derection = 180deg.
Теперь кратко про Radial. `radial-gradient(shape size at position, color1, color2)`. Изначально градиент идет как circle от центра к краям, но можно поменять shape и at position, например radia-`gradient(ellipse 100px at left top, red, blue)` 

## Box Shadow
`box-shadow: offsetX, offsetY, blurRadius, spreadRasius, color`
