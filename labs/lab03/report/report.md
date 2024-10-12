---
## Front matter
title: "Отчет по лабораторной работе №3"
subtitle: ""
author: "Платонов Иван Георгиевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью данной работы является обучение работы с языком разметки MarkDown для упращения написания шаблонных отчетов по лабораторным работам.

# Задание

1. Изучить язык разметки MarkDown;
2. Научиться компилировать его в .pdf и .docx файлы.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

Сначала скачаем изменения из удаленного репозитория.

![Скачивание изменений из удаленного репозитория](image/2.png){#fig:002 width=70%}

Для создания .docx, .pdf файлов, используя язык MarkDown, необходимо использовать команду make, которая запускает в работу скрипт Makefile, который, в свою очередь, запускает pandoc, использующий LateX для верстки документа.

![Создание .docx .pdf файлов на основе верстки](image/1.png){#fig:001 width=70%}

На данном скриншоте видно, как при помощи команды make запускается цепочка скриптов, верстающих документ.

![Проверка на наличие сверстанных файлов](image/3.png){#fig:003 width=70%}

Далее проверяем на наличие сверстанных документов.

![Очистка сверстанных файлов](image/4.png){#fig:004 width=70%}

Удаляем их при помощи make clean.

![Изменение в верстке](image/5.png){#fig:005 width=70%}

Здесь показано, как можно изменять верстку документа.

![Пример верстки отчета по второй лабораторной работе](image/6.png){#fig:006 width=70%}

Пример что-то похожего на верстку отчета по второй лабораторной работе.

# Выводы

К сожалению, я не могу найти данную лабораторную работу полезной для себя по нижеприведенным причинам.

Хоть данная технология и призвана "ускорить" написание отчета по лабораторной работе, фактически теряются уникальность написания отчетов, при этом так же и теряются мультифункциональность и гибкость, представленных в полноценных текстовых процессорах. Автор отчета не обучается писать отчеты в соответствии с ГОСТ-7.32-2017, ГОСТ-2, ГОСТ-7.05-2008 и других - вместо этого ему предоставлен универсальный шаблон, который никак не может развить навыки написания настоящих отчетов.

Возможно, данная работа была направлена для изучения языка верстки, однако в методическом пособии для данной лабораторной работы было сказано лишь о том, как вставить формулу и картинку.

Итогом данной работы можно еще выделить то, что у меня появился pandoc, при помощи которого, я могу теперь конвертировать .md файлы в .pdf файлы. 

Последнее, что хотелось бы сказать, так это то, что данная лабораторная работа была первой и единственной, в которой я пользовался версткой для написания отчета: я обладаю достаточными навыками, знаниями и образованием, чтобы написать отчет по лабораторной работе в соответствии с ГОСТ, пользуясь текстовым процессором, а не автоматизацией, которая явно лично мне вредит.

# Список литературы{.unnumbered}

::: {#refs}
:::
