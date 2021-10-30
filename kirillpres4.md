---
## Front matter
lang: ru-RU
title: Лабораторная работа №4
author: |
	Сидоракин
institute: |
	 RUDN University, Moscow, Russian Federation
date: Сентябрь, 2021 Москва

## Formatting
toc: false
slide_level: 2
theme: metropolis
sansfont: NotoMono-Regular
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---
## Цель лабораторной работы

Получение практических навыков работы в консоли с расширенными атрибутами файлов

## Процесс выполнения лабораторной работы

## Определяем расширенные атрибуты файла

![Расширенные атрибуты](image/1.jpg){ #fig:001 width=50% }

## Устанавливаем на файл права, разрешающие чтение и запись

![Чтение и запись](image/2.jpg){ #fig:002 width=50% }

## Попробуем установить на файл расширенный атрибут "a"
![Расширенный атрибут](image/3.jpg){ #fig:003 width=50% }

## От имени суперпользователя
![Суперпользователь](image/4.jpg){ #fig:004 width=50% }

## Проверяем правильность установления атрибута
![Атрибут](image/5.jpg){ #fig:005 width=50% }

## Выполняем дозапись в файл file1 слова «test» 
![Дозапись](image/6.jpg){ #fig:007 width=50% }

## Считываем файл file1 командой cat  
![Считывание](image/6.1.jpg){ #fig:008 width=50% }

## Попробуем удалить файл file1 либо стереть информацию 
![Удаление и считывание](image/7.jpg){ #fig:009 width=50% }

![Удаление и считывание](image/7.1.jpg){ #fig:010 width=50% }

## Попробуем установить запрет на чтение и запись 

![Чтение и запись](image/8.jpg){ #fig:001 width=50% }

## Снимаем расширенный атрибут "a" от имени суперпользователя 
![Снятие атрибутов](image/9.jpg){ #fig:013 width=50% }

## Повторяем операции, которые нам ранее не удавались
![Повторение](image/9.1.jpg){ #fig:014 width=50% }

## Повторяем действия по шагам, заменив атрибут «a» на «i»
![Дозапись файла](image/10.jpg){ #fig:016 width=50% }

![Изменение прав](image/10.1.jpg){ #fig:016 width=50% }


## Вывод
В результате выполнения работы вы повысили свои навыки использования интерфейса командой строки (CLI), познакомились на примерах с тем, как используются основные и расширенные атрибуты при разграничении доступа.