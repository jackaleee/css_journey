# Pseudo-classes

## 1. User Action
LoVe HAte (link, visited, hover, active) + focus - easy way to remember 
---
__:hover__ - user hover mouse over element <br>
__:active__ - user press on element or hold it <br>
__:focus__ - curson in the input field (or "tab" focus) <br>
__:focus-visible__ - only for keybord focus (tab) <br>
__:focus-within__ - works for parent element, which has focus inside of it (defference between focus and focus-within is that within highlighs parent element, and focus highlights only child element(s) <br>
__:target__ - it styles the element that has an id matching the part of the URL after #. It selects element when it is a target of URL hash <br>
__:enebled__ / :disabled - styles only enabled input elements, disabled work in opposite way, it styles only disabled input elements <br>
:valid / :invalid - without js gives user info about their input, simple validation style <br> 
:in-range / :out-of-range - styles min/max input[type="number/range"] <br>
:read-only / :read-write - useful for input/textarea, it styles element depends on their value in html <br>
:placeholder-shown - when element has a placeholder actual value (placeholder="" not empty)

## 2. Input 
__:required__ / :optional - when field is required, we use the first one. If it doesnt contain required statement, so we can style elements with optional. <br>
__:checked__ - apply styles when checkbox or radio has been selected <br>
__:default__ - is styles default elements, defined with checked or selected in html <br>

## 3. Location
__:any-link__ = :link + :visited - It styles all linlks, even if they have been visited or not. Apply this class when you want to style all links and don't care whether they have been visited or not <br>
__:local-link__ - FIREFOX ONLY (use instead a[href^="#"]) -rare pseudo-class, styles only # links (links follow you on the same page, you are currently see) if you want to style local links differently <br>
__:target-within__ - has all :target functions, but it also applies to parent element <br>

## 4. Tree-structural 
__:root__ = html <br>
__:empty__ - для редакции пустых листов, списков и чего-либо пустого. Пример: `<li></li>`. `ul:empty { displey: none; }` <br>
__:nth-child(n)__ - позволяет выбрать конкретный элемент в родительском контейнере <br>
__:nth-last-child(n)__ - точно так же работает как и nth-child, только отсчет идет с обрантной стороны <br>
__:first-child / :last-child__ - выбирает первого/последнего ребенка в род контейнере <br>
__:only-child__ - выбирает только одиновчный элемент в родителе, который тег которого больше не повторяется в контейнере <br>
<br>
__:fist-of-type / last-of-type__ - выбирает первый или последний элемент своего типа в родителе. В отличии от first/last-child здесь обязательно должен указываться тег элемента. <br>
__:nth-of-type(n)__ - так же как и в nth-child можно выбрать конкретный элемент по нумерации, но только нужно обязательно указывать тег <br>
__:only-of-type__ - выбирает элемент, если он единсвтенный в своем теге в родительском элементе (ОН ТАКОЙ ОДИН) <br>

## 5. Functional
__:is()__ - очень удобный псевдо, позволяет вписать в себя другие селекторы списком. Берет максимальную специфичность. Пример: `:is(h1, h2, h3){` <br>
Осообенно хорошо подходит для более сложных конструкций `nav :is(li, ul) li a { ` <br>
__:where()__ - работает так же, как и :is(), только его специфичность = 0. Про специфичность выкачу пост, чтобы вы могли легко понимать как он работает. Более униваерсальный инструмент <br>
<br>
__:has()__ - чилловый псевдо, который позволяет "посмотреть внутрь" элемиента, то есть "если внутри меня есть Х, то применяй это". Пример: `.class:has(img, a) {`. Может внутри себя принимать еще псевдо. Пример того, как можно подсвечивать label, когда input в фокусе `label:has(input:focus) {` <br>
__:not()__ - отрицательный фильтр, он выбирает все элементы, кроме тех, которые внутри скобок. То есть мы можем исключить что не нужно стилизировать в :not(). То есть укзаываем селектор, который хотим исключить. Пример: `p:not(.class) {`<br>
Все элементы p, кроме тех, у которых класс = class, будут выбраны 

## PSEUDO-ELEMENTS
__::before ::after__ - элементы, которые можно добавить до и после содержимого, например может использоваться для breadcrumb на сайтах. Обязательно использовать `content: " "`. Часто используется для анимаций. <br> <br>
__::first-letter__ - редактировать стиль первой буквы (обычно абзаца) <br> <br>
__::marker__ - позволяет редачить маркеры в списках (цифра, стрелка, точка). Управляет тем что перед li



