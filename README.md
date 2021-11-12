# PureBasketball

Этот проект был разработан [Kanroska](https://github.com/Kanroshka).

## Описание проекта
Проект был создан для людей, которые увлекаются баскетболом или хотят втянуться в этот прекрасный мир.
Для этого было создано приложение, которое может быть полезно как для новичков, так и для людей, которые не впервые слышат, что такое баскетбол и хотят
улучшить свои навыки в этой замечательной игре. Так же использовать данную программу могут пользователи, которые не особо любят играть, но хотят получать последние
новости связанные с миром баскетбола.

## Описание реализации
Для выполнения данной задумки было создано несколько классов, некоторые из которых выполняли роль окон для приложение и их дизайн.
Другие же выполняли роль функционала для этого проекта, например была создана функция под названием 'parser', которая выполняла роль
поиска и сохранение новостей с одного из новостного сайта.

Интересной задачей было решение проблемы, которая происходила после вызова методов  **`grabMouse()`** и **`setMouseTracking(True)`**, так как после вызова этих функций
окно переставло ловить нажатие на кнопки. Данную проблемы я решил с помощью **`mousePressEvent()`**, которая в моей проекте послужила для 'отлова'
нажатий левой кнопки мыши.

![Реализация mousePressEvent](img/for_readme2.png 'Реализация mousePressEven()')

## Описание технологий
Были использованы многочисленные библиотеки, но так как надо было создать GUI, то основа всего проекта написана на ***PyQt5***. Не менее важными были и например:
***BeautifulSoup*** и ***requests***. С помощью которых как раз и был написан скрипт для поиска новостей. Из ***requests*** мне понадобилась функция
**`get(url)`**, которая отправляла GET запросы по данной ей ссылки (url). А с помощью BeautifulSoup и ее метода **`find_all()`** я уже находил нужные мне элементы на HTML странице.

Для того, чтобы добавить регистрацию в приложение была использована библиотека ***sqlite3***. При помощи её я смог сделать сохранение новых пользователей, которые
вписывали login и password, а программа проверяла бы возможность добавления этого человека в базу и вход уже зарегистрированных юзеров.

Так как в моём проекте встречается достаточно много текста, который нужно было вписать самому, я принял решение записывать весь текст в ***.txt*** файле, а потом уже
оттуда с помощью конструкции **`with open() as f:`** считывать все строки. Это решение позволило мне не загрязнять код не нужным текстом. 



## Список всех используемых библиотек
- ***beautifulsoup4***
- ***lxml***
- ***PyQt5***
- ***urllib3***
- ***requests***
- ***sys***
- ***os***
- ***sqlite3***
