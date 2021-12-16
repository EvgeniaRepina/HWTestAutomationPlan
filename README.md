# План автоматизации тестирования функции записи на обучение профессии "Тестировщик ПО" на сайте Netology.ru

**Объект тестирования:** [сайт Нетологии](https://netology.ru/#/).

**Тестируемая функция:** запись на обучение профессии ["Тестировщик ПО"](https://netology.ru/programs/qa).

**Приоритет:** Высокий. Функция записи на обучения реализует одну из основных задач бизнеса — продажа учебных 
программ конечному пользователю.

**Уровни тестирования:** API, UI; Интеграционное, системное.

**Виды тестирования используемые в процессе:**

- Автоматизированное.

- Функциональное, GUI, нефункциональное (безопасности, юзабилити, конфигурационное).

- Комплексное хронологически, по тестам, позитивное/негативное, черного ящика, без 
подробной документации и требований.

**Критерии начала тестирования:** готовность объекта, законченность разработки требуемого функционала,
наличие всей необходимой документации, наличие всех необходимых разрешений и доступов.

**Критерии окончания тестирования:**
результаты тестирования удовлетворяют критериям качества продукта (требования к количеству открытых багов выполнены).

**Окружение** (статистически распространенные в русскоязычном сегменте
интернета версии ):

- телефоны (ОС: Android, iOS, Windows и пр. статистически значимые).

- планшеты (ОС: Windows, OS X, Linux и пр. статистически значимые).

- десктопы (ОС: Windows, OS X, Linux и пр. статистически значимые).

- браузеры: Chrome, Яндекс. Браузер, Safari, Opera, Firefox и пр. статистически значимые.

## Перечень автоматизируемых сценариев.
(см. приоритеты, для принятия решений о сокращении объема, в случае нехватки ресурсов).

**Юзер-сценарий поиска страницы курса «Тестировщик ПО»:**

- Блок «Изучайте актуальные темы»/Ссылка «Программирование» - Список курсов по направлению программирование - 
  Страница курса (средний приоритет).
- Кнопка «Каталог курсов» сверху - Список направлений с выпадающими списками курсов  по уровням - Страница курса 
  (высокий приоритет).
- Кнопка «Каталог курсов» сверху - Ссылка «Полный каталог» - Список всех курсов - Страница курса (высокий приоритет).
- Ссылка «Каталог курсов» в футере - Список всех курсов - Страница курса (низкий приоритет).
- Блок «Выберите вектор Развития» / ссылка «Выбрать курс» - Список всех курсов - Страница курса (средний приоритет).
- Блок «Сделайте шаг ...» / раздел «Нео» - Список Курсов по уровню начинающий  - Страница курса (средний приоритет).

**Юзер-сценарий поиска формы записи на курс на странице курса «Тестировщик ПО»:**

- Кнопка "Записаться" в блоке с информацией о курсе вверху страницы - прокрутка страницы до формы внизу (высокий 
  приоритет).
- Кнопка "Записаться" внутри контента страницы - Форма для записи во всплывающем окне (средний приоритет).
- Прокручивание страницы до формы для записи внизу страницы (высокий приоритет).


**Юзер-сценарий взаимодействия с формой записи на курс «Записаться»:**

- Happy path (высокий приоритет).
- Sad Path. Поля: Имя и Телефон (низкий приоритет).
- Evil Path. Поля: Имя и Телефон (средний приоритет).

**Юзер-сценарий взаимодействия с формой записи на курс «Получить консультацию»:**

- Happy path (высокий приоритет).
- Sad Path. Поля: Имя и Телефон (низкий приоритет).
- Evil Path. Поля: Имя и Телефон (средний приоритет).

## Перечень используемых инструментов с обоснованием выбора.
Все инструменты бесплатны. Довольно широко применяются, знакомы команде проекта (что позволит не нанимать сторонних 
исполнителей), могут применяться одновременно в проекте.

**Система контроля версий:**

**Git.** Небольшой и быстрый. Обеспечивает все необходимые функции в т.ч. резервное копирование, ветвление (управление которым реализовано довольно просто и эффективно).

**Сервис онлайн-хостинга:**

**GitHub.** Удобный интерфейс, интегрирован с Git.

**Язык:**

**Java SE 11 (Java JDK 11).** Автоматизаторы проекта работают на этом языке, он имеет необоходимый и достаточный набор инструментов для автоматизации, имеет удобную экосистему.

**Среда разработки:**

**IntelliJ IDEA.** Удобная среда разработки для Java с поддержкой последних технологий и фреймворков.  Автоматизаторы проекта имеют большой опыт работы в ней.

**Тестовый Фреймворк:**

**JUnit 5.** Удобен, содержит все необходимые для тестирования инструменты.

**Библиотеки, плагины:**

**Selenide.** Библиотека для написания лаконичных и стабильных тестов.

**Lombok.** Позволяет оптимизировать код автотестов, уменьшая усилия на разработку.

**Rest Assured.** Позволяет автоматизировать тестирование get и post запросов, и автоматизировать тестирование REST-API.

**JavaFaker.** Позволяет быстро и просто генерировать данные для тестов.

**Репортинг и CI:**

**Gradle.** Система автоматической сборки и проверки кода, позволяющая автоматически и без участия людей проверять код.
Легка в настройке, позволяет экономить время и пр.ресурсы на проекте.

**Allure.** Дает достаточно информации о похождении тестов и ошибок. Визуально нагляден, позволяет быстро анализировать 
результат и исправлять ошибки в тестах.

## Перечень необходимых разрешений/данных/доступов.
- Разрешение на проведение тестирования сайта Netology.ru.
- Доступ к базе данных сайта Netology.ru.
- Доступ к API сайта Netology.ru.

## Перечень и описание возможных рисков при автоматизации.
- Изменение сайта, его модулей (технического исполнения).
- Изменение стратегии продаж, списка курсов и пр.
- Неверная оценка трудозатрат.
- Увольнение/перераспределение людей.
- Использование рандомных данных, может привести к пропуску багов, закономерностей ведущих к багам.
- Низкая продуктивность, скорость работы.
- Низкое качество работы сотрудников.
- Отзыв разрешений и доступов.
- Изменение требований к продукту.
- Недоступность инструментов, хостинг-площадок и пр.

## Перечень необходимых специалистов для автоматизации.
- Руководитель группы (лид, или сеньор). Роли: архитектура, тест-дизайн, управление (планирование, сбор метрик, 
  анализ результатов).
- Тестировщик-автоматизатор. Роли: тест-дизайн, разработка, тестирование.

## Интервальная оценка с учётом рисков (в часах).

| Сотрудник  | Подготовка |  Тестирование |  Анализ результатов|Итого   |
| :------------ |:---------------:|  :---------------:|  :---------------:|   :---------------:|
| Руководитель     | 5 | 0 |6 |11 |
| Тестировщик-автоматизатор    | 16       |   1       |2       |19       |

**Всего чел./часов:	30**




