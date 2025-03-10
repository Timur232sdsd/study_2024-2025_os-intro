---
## Front matter
title: "Отчёт по лабораторной работе"
subtitle: "Простейший вариант"
author: "Тимур Риантвоич Каримов"

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

Изучить идеологию и применение средств контроля версий.
Освоить умения по работе с git.

# Задание

1. Установка программного обеспечения
2. Базовая настройка git
3. Создайте ключи ssh
4. Создайте ключи pgp
5. Настройка github
6. Добавление PGP ключа в GitHub
7. Настройка автоматических подписей коммитов git
8. Настройка gh
9. Шаблон для рабочего пространства

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

Установка программного обеспечения (рис. [-@fig:001]).

![Установка](image/1.png){#fig:001 width=70%}

Задаем имя и email владельца репозитория и настроим utf-8 в выводе (рис. [-@fig:002]).

![Ввод имя и email](image/2.png){#fig:002 width=70%}

Затем настраиваем верификацию и подписание коммитов, параметр *autocrlf* и *safecrlf* (рис. [-@fig:003]).

![Верификаия комммитов и настройка параметров](image/3.png){#fig:003 width=70%}

Создаем *ssh* ключи  по алгоритму *rsa* (рис. [-@fig:005]) и *ed25519*(рис. [-@fig:004]).

![Создание ключа ssh по алгоритму rsa](image/5.png){#fig:005 width=70%}

![Создание ключа ssh по алгоритму ed25519](image/4.png){#fig:004 width=70%}

Генерируем ключ (рис. [-@fig:006]).

![Генерация ключа](image/6.png){#fig:006 width=70%}

Выводим список ключей (рис. [-@fig:007]).

![Вывод ключей](image/7.png){#fig:007 width=70%}

Вводим код для копирования сгенерированного ключа в буфер обмена, а также настроим автоматические подписи коммитов git (рис. [-@fig:008]).

![Ввод кода для копирования и настройка коммитов git](image/8.png){#fig:008 width=70%}

Затем авторизуемся (рис. [-@fig:009]).

![Авторизация](image/9.png){#fig:009 width=70%}

Создадим шаблон рабочего пространства

Создадим необходимые директории и перейдем в них, затем создадим собственный репозиторий(рис. [-@fig:010]).

![Создание собственного репозитория](image/10.png){#fig:010 width=70%}

Скопируем полученный репозиторий (рис. [-@fig:011]).

![Копирование полученного репозитория](image/11.png){#fig:011 width=70%}

Затем перейдем в каталог курса для удаления лишних файлов и создания необходимых каталогов (рис. [-@fig:012]).

![Удаление лишних файлов и создание необходимых каталогов](image/12.png){#fig:012 width=70%}

Оправим файлы на сервер (рис. [-@fig:013]).

![Отправка файлов на сервер](image/13.png){#fig:013 width=70%}

# Выводы

Упешно настроена рабочая среда для разработки и управления проектами.

Настроены инструмены для работы с Git и GitHub, включая подписание коммитов с использованием PGP.

Создано рабочее пространство на основе шаблона.

# Список литературы{.unnumbered}

::: {#refs}
:::
