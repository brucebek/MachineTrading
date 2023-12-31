# MachineTrading

## Описание проекта
Чат-бот предназначен для предоставления пользователям прогнозов стоимости акций на основе исторических данных и рыночных тенденций и осуществления трейдинга с использованием полученной информации о текущей и предполагаемой стоимости стоков.

## Анализ задания
Задача прогнозирования стоимости акций предполагает анализ больших объемов данных и составление прогнозов относительно будущей стоимости акций на основе рыночных тенденций и других факторов. Для достижения этой цели чат-бот использует алгоритмы машинного обучения. 

Предварительный анализ истории торгов акции представлен в Colab Notebook по ссылке: [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1JuUK_wvtx-wwW2gfIGfndgVOF9INgMlW/view?usp=sharing)

## Требования к проекту
* Поиск акции по введенной пользователем строке
* Интеграция с MOEX API для доступа к данным о стоимости акций
* Анализ временных рядов для прогнозирования будущей стоимости акций
* Реализация функционала трейдинга через телеграм-бот на уровне прототипа
* Удобство и простота в использовании

## Архитектура проекта
* Проект написан на Python.
* Для обработки пользовательского ввода, генерации и вывода ответов использована библиотека _aiogram_
* Для анализа временных рядов — составления прогнозов относительно будущей стоимости акций — использована библиотека _autots_
* Для доступа к данным о стоимости акций реализована интеграция с _MOEX API_
* Хранение общей суммы пополнений баланса, состава портфеля и количества активов реализованы с использованием СУБД _SQLite_
* В качестве площадки для чат-бота используется Telegram.

## Структура проекта

* MoexML: ml-модель + взаимодействие с api биржи
* ChatBot: бот
* DataBase: хранение данных портфелей пользователей
      
## Запуск

    pip install -r requirements.txt
    python -m DataBase.create_db
    python -m ChatBot.app

Бот доступен по ссылке: https://t.me/MachineTraidingBot.
