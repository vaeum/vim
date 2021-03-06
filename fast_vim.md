Все комманды вводяться в коммандном режиме.



- ci' - [c]hange [i]n ' (одинарная ковычка)


- ciw - [c]hange [i]n [w]ord - удаляет полностью слово, даже если вы нахотесь в его середине


- cit - [c]hange [i]n [t]ag - HTML и XML писатели полюбят эту комманду - удаляет содержимое тега, в котором находится курсор.

### Примечание

Клавиша <leader> по умолчанию это **[\]**

| Перемещение по документу               | Команды VIM       |
| -------------------------------------- | ----------------- |
| Как переместиться *вниз*?              | **j**             |
| Как переместиться *влево*?             | **h**             |
| Как переместиться *вправо*?            | **l**             |
| Как переместиться *вверх*?             | **k**             |
| Как переместиться *в конец строки*?    | **$ (shift + 4)** |
| Как переместиться *в начало строки*?   | **^ (shift + 6)** |
| Как переместиться *в начало слова*?    | **w**             |
| Как переместиться *в конец слова*?     | **e**             |
| Как переместиться *в начало экрана*?   | **H (shift + h)** |
| Как переместиться *в середину экрана*? | **M (shift + m)** |
| Как переместиться *в конец экрана*?    | **L (shift + l)** |

| Прокрутка в текущем окне      | Команды VIM |
| ----------------------------- | ----------- |
| Проскроллить экран вверх      | **zt**      |
| Проскроллить экран в середину | **zz**      |
| Проскроллить экран в низ      | **zb**      |

| Команды с переходом в режим вставки | Команды VIM |
| ----------------------------------- | ----------- |
| Удалить слово                       | **cw**      |

В режиме вставки можно удалять текст следующими комбинациями клавишами:

| Команды с переходом в режим вставки      | Команды VIM        |
| ---------------------------------------- | ------------------ |
| Удалить символ                           | **<C-h> (ctrl-h)** |
| Удалить слово                            | **<C-w> (ctrl-w)** |
| Удалить текст от курсора до конца строки | **<C-u> (ctrl-u)** |

| Редактирование                           | Команды VIM                |
| ---------------------------------------- | -------------------------- |
| Как вы переместите курсор вниз на строк 7 ? | **7j**                     |
| Как вы удалите слово Именно слово ?      | **dw**                     |
| Как вы ищете в файле слово на котором в данный, момент находится курсор ? | *                          |
| Как произвести поиск и замену только в строках с 50 по 100 ? | **:50,100s/old/new/g**     |
| Что делать если вы хотите посмотреть две разные, части одного и того же файла одновременно ? | **:sp**                    |
| Что делать если вы хотите выбрать лучшую, цветовую схему дисплея ? | **:colorscheme desert**    |
| Что делать если вы хотите чтобы сочетание клавиш Ctrl-S сохраняло файл ? | **:nmap \<c-s\> :w\<CR\>** |
| Что делать если вы хотите открыть файл имя , , которого прописано в текущем документе и курсор стоит на нем ? | **gf**                     |
| Как удалить с текущей позиции и до конца файла? | **dG**                     |
| Как удалить с текущей позиции и до начала файла? | **dgg** или **d1G**        |

