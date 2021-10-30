---
# Front matter
title: "Лабораторнаяработа № 4"
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя"
author: "Сидоракин Кирилл Вячеславович НБибд-01-18"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=070 # the penalty for breaking a line at a binary operator
  - \relpenalty=050 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=010 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
  - \usepackage{rotating}
  - \usepackage{tabularx}
---

# Цель работы

Получение практических навыков работы в консоли с расширенными атрибутами файлов

# Выполнение лабораторной работы

1.От имени пользователя guest определяем расширенные атрибуты файла
![Расширенные атрибуты](image/1.jpg){ #fig:001 width=50% }

2.Устанавливаем командой "chmod 600 file1" на файл file1 права, разрешающие чтение и запись для владельца файла
![Чтение и запись](image/2.jpg){ #fig:002 width=50% }

3.Попробуем установить на файл "/home/guest/dir1/file1" расширенный атрибут a от имени пользователя guest
![Расширенный атрибут](image/3.jpg){ #fig:003 width=50% }

4.Попробуем установить расширенный атрибут a на файл "/home/guest/dir1/file1" от имени суперпользователя
![Суперпользователь](image/4.jpg){ #fig:004 width=50% }

5.От пользователя guest проверьте правильность установления атрибута
![Атрибут](image/5.jpg){ #fig:005 width=50% }

6.Выполняем дозапись в файл file1 слова «test» 
![Дозапись](image/6.jpg){ #fig:007 width=50% }

Считываем файл file1 командой cat "/home/guest/dir1/file1" 
![Считывание](image/6.1.jpg){ #fig:008 width=50% }

7.Попробуем удалить файл file1 либо стереть имеющуюся в нём информацию 
![Удаление и считывание](image/7.jpg){ #fig:009 width=50% }

![Удаление и считывание](image/7.1.jpg){ #fig:010 width=50% }

8.Попробуем установить на файл file1 права запрещающие чтение и запись для владельца файла
![Чтение и запись](image/8.jpg){ #fig:001 width=50% }

9.Снимаем расширенный атрибут "a" с файла от имени суперпользователя командой 
![Снятие атрибутов](image/9.jpg){ #fig:013 width=50% }

Повторяем операции, которые вам ранее не удавалось выполнить
![Повторение](image/9.1.jpg){ #fig:014 width=50% }

10.Повторяем наши действия по шагам, заменив атрибут «a» атрибутом «i»
![Дозапись файла](image/10.jpg){ #fig:016 width=50% }

![Изменение прав](image/10.1.jpg){ #fig:016 width=50% }

# Вывод

В результате выполнения работы вы повысили свои навыки использования интерфейса командой строки (CLI), познакомились на примерах с тем, как используются основные и расширенные атрибуты при разграничении доступа. Имели возможность связать теорию дискреционного разделения доступа (дискреционная политика безопасности) с её реализацией на практике в ОС Linux. Составили наглядные таблицы, поясняющие какие операции возможны при тех или иных установленных правах. Опробовали действие на практике расширенных атрибутов «а» и «i».