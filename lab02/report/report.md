---
# Front matter
lang: ru-RU
title: "Лабораторная работа №2"
subtitle: "Задача о погоне (18 вариант)"
author: "Никитаева Александра Семеновна"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Научиться решать задачу о погоне, строить графики траектории движения, выводить уравнение, описывающее движение.

# Задание

На море в тумане катер береговой охраны преследует лодку браконьеров. Через определенный промежуток времени туман рассеивается, и лодка обнаруживается на расстоянии 7,7 км от катера. Затем лодка снова скрывается в тумане и уходит прямолинейно в неизвестном направлении. Известно, что скорость катера в 3,3 раза больше скорости браконьерской лодки.

  1. Запишите уравнение, описывающее движение катера, с начальными условиями для двух случаев (в зависимости от расположения катера относительно лодки в начальный момент времени).
  2. Постройте траекторию движения катера и лодки для двух случаев.
  3. Найдите точку пересечения траектории катера и лодки 

# Выполнение лабораторной работы

## Постановка задачи
1. Место нахождения лодки браконьеров в момент обнаружения: $t_0 = 0, x_{л0} = 0$
. Место нахождения катера береговой охраны относительно лодки браконьеров в момент обнаружения лодки: $x_{к0} = 0$


2. Введем полярные координаты. Считаем, что полюс - это точка обнаружения лодки браконьеров $x_{л0} (\theta = x_{л0} = 0)$
, а полярная ось r проходит через точку нахождения катера береговой охраны (рис. -@fig:001)

![Положение катера и лодки в начальный момент времени](image/1.png){ #fig:001 width=70% }

3. Траектория катера должна быть такой, чтобы и катер, и лодка все время были на одном расстоянии от полюса, только в этом случае траектория катера пересечется с траекторией лодки. Поэтому для начала катер береговой охраны должен двигаться некоторое время прямолинейно, пока не окажется на том же расстоянии от полюса, что и лодка браконьеров. После этого катер береговой охраны должен двигаться вокруг полюса удаляясь от него с той же скоростью, что и лодка браконьеров.


4. Чтобы найти расстояние $X$ (расстояние, после которого катер начнет двигаться вокруг полюса), необходимо составить простое уравнение. Пусть через время t катер и лодка окажутся на одном расстоянии $x$ от полюса. За это время лодка пройдет $x$, а катер — $k - x$ (или $k + x$ в зависимости от начального положения катера относительно полюса). Время, за которое они пройдут это расстояние, вычисляется как $\frac{x}{v}$ или $\frac{k-x}{3.3v}$ (во втором случае $\frac{k+x}{3.3v}$). Так как время одно и то же, то эти величины одинаковы. Тогда неизвестное расстояние $x$ можно найти из следующего уравнения:
$$ \frac{x}{v} = \frac{k-x}{3.3v}\ в\ первом \ случае$$
или
$$ \frac{x}{v} = \frac{k+x}{3.3v}\ во\ втором.$$

Отсюда мы найдем два значения $x_1 = \frac{10}{43}k$ и $x_2 = \frac{10}{23}k$ 
, задачу будем решать для двух случаев.


5. После того, как катер береговой охраны окажется на одном расстоянии от полюса, что и лодка, он должен сменить прямолинейную траекторию и начать двигаться вокруг полюса, удаляясь от него со скоростью лодки $v$. Для этого скорость катера раскладываем на две составляющие: $v_r$ — радиальная скорость и $v_{\tau}$ — тангенциальная скорость (рис. 2). Радиальная скорость - это скорость, с которой катер удаляется от полюса, $v_r = \frac{dr}{dt}$. Нам нужно, чтобы эта скорость была равна скорости лодки, поэтому полагаем $\frac{dr}{dt}=v$.

Тангенциальная скорость – это линейная скорость вращения катера относительно полюса. Она равна произведению угловой скорости $\frac{\partial \theta}{\partial t}$ на радиус $r,\ v_{\tau} = r \frac{\partial \theta}{\partial t}$

Из рисунка (рис. -@fig:002) видно: $v_{\tau} = \sqrt{10.89^2 - v^2} = \sqrt{9.89}v$ (учитывая, что радиальная скорость равна $v$). Тогда получаем $r \frac{\partial \theta}{\partial t} = \frac{\sqrt{989}}{10}v$

![Скорости](image/2.png){ #fig:002 width=70% }

6. Решение исходной задачи сводится к решению системы из двух дифференциальных уравнений: 

\begin{equation*} 
  \begin{cases} 
    \frac{\partial r}{\partial t} = v 
    \\
    r \frac{\partial \theta}{\partial t} = \frac{\sqrt{989}}{10}v 
  \end{cases}
\end{equation*} 

с начальными условиями 

\begin{equation*}
  \begin{cases}
    \theta_0 = 0 
    \\ 
    r_0 = x_1 
  \end{cases}
\end{equation*}

\begin{equation*}
  \begin{cases}
    \theta_0 = -\pi
    \\
    r_0 = x_2
  \end{cases}
\end{equation*} 

Исключая из полученной системы производную по $t$, можно перейти к следующему уравнению:
$$ \frac{\partial r}{\partial \theta} = \frac{10r}{\sqrt{989}}.$$
Начальные условия остаются прежними. Решив это уравнение, мы получим траекторию движения катера в полярных координатах.

## Построение траектории движения и точки пересечения
Код для первого случая на python:

```
k = 7,7 км -- расстояние от катера, на котором обнаруживается лодка
Vк = 3,3Vл

k = 18.2
fi = 3*math.pi/4

Начальные условия:
1) te0 = 0, r0 = 10/43*k
2) te0 = -pi, r0 = 10/23*k

def dr(r, tetha): #функция, описывающая движение катера береговой охраны
    dr = 10*r/math.sqrt(989)
    return dr

r01 = 10/43*k #1 случай
r02 = 10/23*k #2 случай

te = np.arange(0, 2*math.pi, 0.01)

r1 = odeint(dr, r01, te)
r2 = odeint(dr, r02, te)

def xt(t): #функция, описывающая движение лодки браконьеров
    xt = math.tan(fi)*t
    return xt

t = np.arange(0, 20, 1)

#Перевод в полярные координаты
tete = (np.tan(xt(t)/t))**-1
rr = np.sqrt(t*t + xt(t)*xt(t))

# Графики
plt.polar(te, r1, 'g') #построение траектории движения катера в полярных координатах. 1 случай
plt.polar(tete, rr, 'b') #построение траектории движения лодки в полярных координатах

plt.polar(te, r2, 'g') #построение траектории движения катера в полярных координатах. 2 случай
plt.polar(tete, rr, 'b') #построение траектории движения лодки в полярных координатах
```

Графики движения и точки пересечения. Зелёным цветом — охрана, синим — браконьеры.

Случай первый (рис. -@fig:003)

![1](image/3.png){ #fig:003 width=70% }

Случай второй (рис. -@fig:004)

![2](image/4.png){ #fig:004 width=70% }

# Выводы

  1. Записала уравнение, описывающее движение катера, с начальными условиями для двух случаев (в зависимости от расположения катера относительно лодки в начальный момент времени).
  2. Построила траекторию движения катера и лодки для двух случаев.
  3. Нашла точку пересечения траектории катера и лодки 
  4. Научилась решать задачу о погоне, строить графики.