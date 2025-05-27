# Pseudo-classes

## 1. User Action
LoVe HAte (link, visited, hover, active) + focus - easy way to remember 
---
:hover - user hover mouse over element <br>
:active - user press on element or hold it <br>
:focus - curson in the input field (or "tab" focus) <br>
:focus-visible - only for keybord focus (tab) <br>
:focus-within - works for parent element, which has focus inside of it (defference between focus and focus-within is that within highlighs parent element, and focus highlights only child element(s) <br>
:target - it styles the element that has an id matching the part of the URL after #. It selects element when it is a target of URL hash <br>
:enebled / :disabled - styles only enabled input elements, disabled work in opposite way, it styles only disabled input elements <br>
:valid / :invalid - without js gives user info about their input, simple validation style <br> 
:in-range / :out-of-range - styles min/max input[type="number/range"] <br>
:read-only / :read-write - useful for input/textarea, it styles element depends on their value in html <br>
:placeholder-shown - when element has a placeholder actual value (placeholder="" not empty)

## 2. Input 
:required / :optional - when field is required, we use the first one. If it doesnt contain required statement, so we can style elements with optional. <br>
:checked - apply styles when checkbox or radio has been selected <br>
:default - is styles default elements, defined with checked or selected in html <br>

## 3. Location
:any-link = :link + :visited - It styles all linlks, even if they have been visited or not. Apply this class when you want to style all links and don't care whether they have been visited or not <br>
:local-link - FIREFOX ONLY (use instead a[href^="#"]) -rare pseudo-class, styles only # links (links follow you on the same page, you are currently see) if you want to style local links differently <br>
:target-within - has all :target functions, but it also applies to parent element <br>

## 4. Tree-structural 
:root = html <br>
:empty - для редакции пустых листов, списков и чего-либо пустого. Пример: `<li></li>`. `ul:empty { displey: none; }` <br>
:nth-child(n) - позволяет выбрать конкретный элемент в родительском контейнере <br>
:nth-last-child(n) - точно так же работает как и nth-child, только отсчет идет с обрантной стороны <br>
:first-child / :last-child - выбирает первого/последнего ребенка в род контейнере <br>
:only-child - выбирает только одиновчный элемент в родителе, который тег которого больше не повторяется в контейнере <br>
<br>
:fist-of-type / last-of-type - выбирает первый или последний элемент своего типа в родителе. В отличии от first/last-child здесь обязательно должен указываться тег элемента. <br>
:nth-of-type(n) - так же как и в nth-child можно выбрать конкретный элемент по нумерации, но только нужно обязательно указывать тег <br>
:only-of-type - выбирает элемент, если он единсвтенный в своем теге в родительском элементе (ОН ТАКОЙ ОДИН) <br>

## 5. Functional
:is() - очень удобный псевдо, позволяет вписать в себя другие селекторы списком. Берет максимальную специфичность. Пример: `:is(h1, h2, h3){` <br>
Осообенно хорошо подходит для более сложных конструкций `nav :is(li, ul) li a { ` <br>
:where() - работает так же, как и :is(), только его специфичность = 0. Про специфичность выкачу пост, чтобы вы могли легко понимать как он работает. Более униваерсальный инструмент <br>
<br>
:has()



