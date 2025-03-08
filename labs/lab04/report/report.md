---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Простейший вариант"
author: "Тимур Ринатович Каримов"

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

Освоение навыков правильной работы с репозиториями git.

# Задание

Установка git-flow
Установка Node.js
Настройка Node.js
Общепринятые коммиты
Создание репозитория git
Работа с репозиторием git

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

Установим *gitflow* (рис. [-@fig:001])

![Установка gitflow](image/1.png){#fig:001 width=70%}

Установим *nodejs* (рис. [-@fig:002]).

![Установка nodejs](image/2.png){#fig:002 width=70%}

Установим *pnpm* (рис. [-@fig:003]).

![Установка pnpm](image/3.png){#fig:003 width=70%}

Запустим *pnpm* (рис. [-@fig:004]).

![Запуск pnpm](image/4.png){#fig:004 width=70%}

Выполненим команду *source ~/.bashrc* (рис. [-@fig:005]).

![Выполнение команды source](image/5.png){#fig:005 width=70%}

Введем программу для помощи в форматировании коммитов (рис. [-@fig:006]).

![Выполнение команды commitizen](image/6.png){#fig:006 width=70%}

Введем программу для помощи в создании логов (рис. [-@fig:007]).

![Выполнение команды standard-changelog](image/7.png){#fig:007 width=70%}

Создадим пустой репозиторий *git-extended* (рис. [-@fig:008]).

![Пустой репозиторий](image/8.png){#fig:008 width=70%}

Сделаем первый коммит и выложим на *GitHub* (рис. [-@fig:009]).

![Коммит и отправка на GitHub](image/9.png){#fig:009 width=70%}

Добавим в файл package.json команду для формирования коммитов (рис. [-@fig:010]).

![Изменения данных в package.json](image/10.png){#fig:010 width=70%}

Добавим новые файлы и выполним коммит (рис. [-@fig:011]).

![Добавление новых файлов и выполнение коммит](image/11.png){#fig:011 width=70%}

Отправим файлы на GitHub (рис. [-@fig:012]).

![Отправка файлов](image/12.png){#fig:012 width=70%}

Инициализируем git-flow (рис. [-@fig:013]).

![Инициализация git-flow](image/13.png){#fig:013 width=70%}

Проверим, что мы на ветке *develop* (рис. [-@fig:014]).

![Проверка ветки](image/14.png){#fig:014 width=70%}

Загрузим весь репозиторий в хранилище (рис. [-@fig:015]).

![Отправка репозитория](image/15.png){#fig:015 width=70%}

Создадим релиз с версией 1.0.0 (рис. [-@fig:016]).

![Создание релиза 1.0.0](image/16.png){#fig:016 width=70%}

Создадим журнал изменений (рис. [-@fig:017]).

![Создание журнала изменений](image/17.png){#fig:017 width=70%}

Добавим журнал изменений в индекс (рис. [-@fig:018]).

![Добавление журнала изменений в индекс](image/18.png){#fig:018 width=70%}

Зальём релизную ветку в основную ветку (рис. [-@fig:019]).

![Отправка релизной ветки в основную](image/19.png){#fig:019 width=70%}

Отправим данные на *GitHub* (рис. [-@fig:020]) и (рис. [-@fig:021]).

![Отправка данных на сервер](image/20.png){#fig:020 width=70%}

![Отправка данных на сервер](image/21.png){#fig:021 width=70%}

Создадим релиз на github. Для этого будем использовать утилиты работы с github (рис. [-@fig:022]).

![Создание релиза на GitHub](image/22.png){#fig:022 width=70%}

Создадим ветку для новой функциональности (рис. [-@fig:023]).

![Создание ветки для новой функциональности](image/23.png){#fig:023 width=70%}

Созданим релиз git-flow (рис. [-@fig:024]).

![Создание релиза git-flow](image/24.png){#fig:024 width=70%}

Обновим номер версии в файле package.json (рис. [-@fig:025]).

![Обновление номера версии в файле package.json](image/25.png){#fig:025 width=70%}

Создадим журнал изменений (рис. [-@fig:026]).

![Создание журнала изменений](image/26.png){#fig:026 width=70%}

Добавим журнал изменений в индекс и создадим релиз на github с комментарием из журнала изменений (рис. [-@fig:029]).

![Создание релиз на github](image/29.png){#fig:029 width=70%}

# Выводы

Работа продемонстрировала эффективность использования современных инструментов разработки, таких как git-flow, commitizen, standard-changelog и pnpm, для автоматизации и стандартизации процессов разработки. Все задачи были выполнены успешно, репозиторий настроен для дальнейшей работы, а процесс создания коммитов, управления ветками и выпуска релизов стал более структурированным и удобным.

# Список литературы{.unnumbered}

::: {#refs}
:::
