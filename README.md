# Заметки о vim

## Окна и буферы

В vim 7 появились табы — привычный способ навигации по файлам. Когда я работал в eclipse я не раз замечал, что часто скакать между табами не удобно, а знакомство с буферами в emacs натолкнуло на прочтение документации по окнам/буферам в vim.

И так, буфер это некий сеанс редактирования определённого файла. К примеру если вы открыли .vimrc и в запущенном виме выполнели :e .bashrc, то откроется .bashrc. Тем не менее буфер с .vimrc останется открытым и доступным для редактирования. Вот основные команды для работы с буферами:

**:bn** следующий буфер
**:bp** предыдущий
**:ls** просмотреть открытые буферы
**:b имя_буфера** переключиться на буфер, очень удобно комбинируется с табом, к примеру пишем :b domain, жмём таб и нам подставляется открытый iis_domain.cpp
**:bd** удалить текущий буфер, правда стоит заметить, что если этот буфер единственное окно то vim закроется
**:bd имя_буфера** удалить буфер по имени

Чем хороши буферы по сравнению с табами? Во первых в vim табы — это теже буферы, только навигация по ним проходит по иному. Проблема табов в том, что они нацелены на визуальную навигацию, а когда вы увлечённо программируете в vim, вам как и мне наверное лень тянуться до мыши и вы точно знаете какой файл хотите редактировать, пишите :b имя — и всё! Ну это конечно же моё имхо :)

С буферами разобрались, поехали дальше. Как я сказал в первом абзаце — иногда нужно часто скакать между файлами, и не табы не буферы просто так проблему не решают. Гораздо удобнее было бы разбить окно на два по вертикали или горизонтали. Сразу из места в карьер, боевой пример: вам нужно узнать определение какой-то функции, если тэги сгенерированны, то достаточно нажать Ctrl-] чтобы перейти на него. Но откроется новый буфер, что не очень удобно. Если же нажать Ctrl-w ] то окно будет разбито по вертикали, и в новом окне будет определение.
Удобно? Мне да. Окошко можно закрыть старым добрым :q или удалить буфер :bd. Чтобы сделать окно единственным (читай развернуть), то выполняем комбинацию Ctrl-w o. Краткое описание работы с окнами:

**Ctrl-w стрелочки :)** — переместиться на окно влево/вправо/вверх/вниз
**Сtrl-w o** — развернуть окно
**Ctrl-w c** — закрыть
**Ctrl-w s** — разделить окно по горизонтали
**Ctrl-w v** — тоже, только по вертикали
**Ctrl-w ]** — разделить и перейти на определение чего-то, что под курсором
**Ctrl-w f** — разделить и в новом окне открыть файл путь к которому находится под курсором, очень удобно делать на инклюдах

Команды:

**:split** — разделить, если указан файл то открыть его
**:vsplit** — тоже только по вертикали
**:sb[uffer]** — разделить и редактировать буффер. Важный момент: если заново открыть файл (к примеру через :split) то буфер сбрасывается, вместе с историей отмен и положением курсора

Собственно про навигацию в vim рассказал всё, что хотел, за помощью обращайтесь в :help window. Хочу лишь добавить про дополнение текста.

Дополнение в vim делается по Ctrl-n, Ctrl-p. Но мы можем указать какой тип дополнений хотим увидеть:

**Ctrl-x Ctrl-f** — файлы, они ищутся в текущем каталоге
**Ctrl-x Ctrl-d** — дефайны
**Ctrl-x Ctrl-i** — слова из текущего и открытых файлов
**Ctrl-x Ctrl-k** — из словаря
**Ctrl-x Ctrl-]** — все тэги
**Ctrl-x Ctrl-o** — omni completion, эдакий intellisense который работает замечательно с C, Python и т.д. но для работы C++ нужен сторонний плагин. Рекомендую.

Надеюсь был полезен.

[https://habrahabr.ru/post/28572/](https://habrahabr.ru/post/28572/)



