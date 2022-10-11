# Прототип рекомендательной системы рецептов (и соответствующий телеграм-бот для взаимодействия с пользователем)
2 варианта работы программы: 1) дает прогноз о вкусовом сочетании имеющихся у пользователя продуктов, их нутриентах и дает ссылки на подходящие рецепты 2) составляет разное меню на каждый день со ссылками на рецепты , данными по ингредиентам и пищевой ценности  предлагаемых блюд

## Содержание

1. [Глава I](#глава-i) \
    1.1. [Цели](#Цели)
2. [Глава II](#глава-ii) \
    2.1. [Что делает данная программа](#Что-делает-данная-программа)
3. [Глава III](#глава-iii) \
    3.1. [Исследования](#Исследования)
4. [Глава IV](#глава-iv) \
    4.1. [Запуск и работа программы](#Запуск-и-работа-программы)
5. [Глава V](#глава-v) \
    5.1. [Запуск телеграм-бота](#Запуск-телеграм-бота)

   

## Глава I
### Цели

Правильно питание - это основа здоровья человека. Организму нужны белки, углеводы и жиры, а также различные микроэлементы.
Первая проблема заключается в том, что наше питание не так разнообразно, как должно было быть.
Вторая проблема состоит в том, что мы любим вкусную, но не полезную еду: картофель фри, чипсы и тому подобное. 
Третья проблема заключается в том, что мы не знаем достаточное количество рецептов вкусных блюд, полезных для здоровья.

Что, если бы у нас было приложение, которое могло бы информировать нас о том, насколько вкусным может быть блюдо, приготовленное из продуктов из нашего холодильника, и какие питательные вещества оно будет содержать, а также могло бы рекомендовать нам рецепты блюд, одновременно полезных и вкусных? Думаю, также было бы здорово, если бы данное приложение могло бы еще и составлять для нас разнообразное меню полезных и вкусных блюд на каждый день.

## Глава II
### Что делает данная программа

Основная программа представляет собой скрипт на языке Python (`nutritionist.py`).
1. Она принимает на вход список ингредиентов.
2. Она создает прогноз и выдает рейтинг с оценкой (`невкусное`, `нормальное`, `вкусное`) блюда, которое можно приготовить на основе списка переданных ингредиентов.
3. Она находит и выводит информацию обо всех питательных веществах (белках, жирах, натрии и т. д.) продуктов из списка, а также их объем в процентах от суточной нормы потребления.
4. Она отображает три рецепта блюд, в которых используется максимальное количество продуктов из списка, с указанием их оценки и ссылок, по которым пользователь сможет найти полную информацию.

Второй вариант работы программы (`nutritionist.py menu`) заключается в следующем:
1. Предлагает соответствующие рецепты для завтрака, обеда и ужина (с ссылками для более подробного описания).
2. При каждом запуске программы рецепты обновляются.
3. Кроме ссылок на предлагаемые рецепты программа выводит также основную информацию по рецепту: 
рейтинг, список необходимых ингредиентов и долю основных нутриентов от суточной нормы потребления.
4. Предлагаемые рецепты имеют рейтинг 4 или 5 из 5.

Также пользователь может запустить данную программу через соответсвующий телеграм-бот.

## Глава III
### Исследования

## Глава IV
### Запуск и работа программы

Для запуска программы скачайте файлы из данного репозитория.

Также установите библитеки из файла requirements.txt: pip install -r requirements.txt

Для основной программы введите в командной строке: python nutritionist.py

Далее программа запросит ввести ингредиенты (на английском языке).

Для второго варианта работы программы - получения дневного меню с рандомными рецептами введите в командной строке: python nutritionist.py menu

## Глава V
### Запуск телеграм-бота

 - Для работы через телеграм-бот получите от BotFather токен (API ключ) и вставьте его в скрипт в указанном месте в файл telebot_nutritionist.py
 - Установите библиотеку PyTelegramBotAPI: pip install PyTelegramBotAPI
 - Запустите данный скрипт в командной строке: python telebot_nutritionist.py
