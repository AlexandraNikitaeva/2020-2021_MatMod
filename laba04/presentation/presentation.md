---
## Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №4"
author: |
	Nikitaeva Alexandra Semenovna\inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
date: 02 March, 2021 Moscow, Russian Federation

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# **Прагматика выполнения лабораторной работы**

## Зачем?

А затем, что каждый, занимающийся математическим моделированием, должен уметь:

* Использовать математический аппарат для решения задач
* Моделировать задачи

# **Цель выполнения лабораторной работы**

## Цель

Построить модель гармонических колебаний с помощью Python.

# **Задачи выполнения лабораторной работы**

## Задание. Вариант 18

Постройте фазовый портрет гармонического осциллятора и решение уравнения гармонического осциллятора для следующих случаев:

1. Колебания гармонического осциллятора без затуханий и без действий внешней силы $\ddot {x} + 13x = 0$

2. Колебания гармонического осциллятора c затуханием и без действий внешней силы $\ddot {x} + 7 \dot {x} + x = 0$

3. Колебания гармонического осциллятора c затуханием и под действием внешней силы $\ddot {x} + \dot {x} + 30x = sin (0,6t)$

На интервале $t \in [0; 57]$ (шаг 0,05) с начальными условиями $x_0 = 0,7, y_0 = 1,5$

# **Результаты выполнения лабораторной работы**

## График колебаний без затуханий и без действий внешней силы

![](image/1.png){ #fig:001 width=70% } 

## График колебаний c затуханием и без действий внешней силы

![](image/2.png){ #fig:002 width=70% }

## График колебаний c затуханием и под действием внешней силы

![](image/3.png){ #fig:003 width=70% }

## Выводы

Построила модель гармонических колебаний с помощью Python.

## {.standout}

Спасибо за внимание!