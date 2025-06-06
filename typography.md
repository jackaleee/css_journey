## Typography 

Typeface - семейство шрифтов <br>
Font - конкретный стиль 

Так же у шрифтов есть возможность менять width, weight (bold, bolder, lighter (или от значение 100-900)), style (italic)

## Font Family

`font-family:` - какой шрифт будет на странице. Лучше указывать сразу несколько вариантов и использовать Web-safe fonts.
А в конце обязательно указывать Generic Font Family. К примеру `sans-serif`. Пример: <br>
`font-family: Arial, "Open Sans", sans-serif` - шрифты состоящий из двух слов должен быть в ковычках. Они подгружаются поочередно в приоритете списка, если нет одного, то идет следующий.

## @font-face 

Это правило позволяет подключить кастомный шрифт и не зависеть от шрифтов, которые установлены у юзера. <br>

`@font-face {
font-family: "MyCustomFont";
src: url("path/to/font.woff2") format("woff2");
}`

Можно добавлять несколько `scr` в разных форматах. 

## External Fonts

Буквально внешние шрифты, которые можно подгрузить с сервака или локала. Например с [Google Fonts](https://fonts.google.com/) через <link> или @import
