## Курсовой проект по дисциплине "Проектирование информационных систем"

## Журавлев Д.А., ИДБ-17-06

### 1. Определение требований к модели [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

**Тема ВКР:** Разработка СУБД для хранения и анализа состояний оборудования и производственных процессов из различных отраслей машиностроительного производства

**Объект исследований:** современное машиностроительное производство

**Предмет исследований:** состояния оборудования и производственных процессов из различных отраслей машиностроительного производства

**Процессы верхнего уровня:** [✋](https://github.com/stankin/design-part-2/wiki/sem1)
* **А1** Управление производством 
* **А2** Подготовка производства к сбору данных
* **А3** Подготовка оборудования
* **А4** Сбор данных
* **A5** Анализ данных

**Точка зрения:** Инженер-технолог

**Цель моделирования:** Определение автоматизируемых функций

### 2. Функциональное моделирование процессов (IDEF0) [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

* A-0 

![A-0](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A0.PNG)

* A0 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/1A0.PNG)

* Декомпозиция A2 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A2.PNG)

* Декомпозиция A3 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A3.PNG)

* Декомпозиция A4 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A4.PNG)

* Декомпозиция A5

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A5.PNG)

### 3. Функциональное моделирование программных и информационных средств (DFD) [✋](https://github.com/stankin/design-part-2/wiki/LR-2)

**Конфигурация технических средств:** ПК; Операционная система Windows 10

**Конфигурация программных средств:** Многоуровневая

**Допустимые виды хранилищ и их размещение:** База данных

* A43 Автоматизация процесса А43

![A43](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A43.PNG)

* A51 Автоматизация процесса А51

![A51](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/A51.PNG)


### 4. Описание выбранного процесса [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате прецедента (Use Case) [✋](https://github.com/stankin/design-part-2/wiki/LR-4)

* [Диаграмма UML Use Case:](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/usecase.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/usecase.png)

**4.1 Идентификатор прецедента:** A5

**4.2 Название прецедента:** Анализ данных

**4.3 Контекст:** A0 СУБД для хранения и анализа состояний оборудования и производственных процессов из различных отраслей машиностроительного производства

**4.4 Участники (actors) и цели (goals):**

| Участник  | Категория  | Цель (goal) |
|---|---|---|
|Администратор | Основной  | Фиксация данных о состоянии оборудования и п/п |
| Инженер-технолог | Основной  | Анализ и мониторинг данных |

**4.5 Предусловия (pre-conditions):**
* Установлена СУБД и создана БД
* Собраны и зафиксированы данные

**4.6 Постусловия (post-conditions):**

* Проанализированные данные о состоянии оборудования и производственных процессов

**4.7 Основной поток выполнения (main flow)**:

| Участник  | Действие (activity)  | Ожидаемый результат |
|---|---|---|
| Инженер-технолог | Получает зафиксированные данные о состоянии оборудования и производственных процессов | Исправное оборудование и отсутствие ошибок в п/п |
| Инженер-технолог | Проводит анализ данных | Полученные результаты анализа |
| Инженер-технолог | Проводит мониторинг данных | Полученное описание текущих и планируемых состояний |
| Инженер-технолог | Формирует отчеты | Проанализированные данные о состоянии оборудования и производственных процессов |

**4.8 Исключения (exceptions):**

| Условие (риск) | Последствия | Реакция |
|---|---|---|
| Ошибка фиксации данных | Невозможность фиксации данных о состоянии оборудования/пп | Осуществление повторного сбора данных |

**4.9 Альтернативы (alternates):**
Не предусмотрено

**4.10 Временные параметры:**

* **Триггер (событие, стартующее прецедент):** Проверка состояния оборудования/производственного процесса

* **Номинальная частота повторения прецедента:** 2 раза в месяц

* **Продолжительность прецедента:** 2 часа

### 5. Описание структуры объекта [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате ERD (Class) [✋](https://github.com/stankin/design-part-2/wiki/LR-5)

* **Описываемый объект:** описание ролей, модулей приложения для работы с СУБД для хранения и анализа данных о состоянии оборудования и производственных процессов

* [ER-диаграмма ролей](https://github.com/ZhuravlevD/projectIS/blob/main/scr/Er-role.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr/Er-role.png)
* [ER-диаграмма модулей](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/ermod.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/ermod.png)

### 6. Описание алгоритма [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Sequence) [✋](https://github.com/stankin/design-part-2/wiki/LR-6)

* **Описываемые процессы и потоки данных:** Создание БД, обработка и анализ данных, проверка корректности данных, заполнение БД, Отоброжание данных в приложении
* [Диаграмма UML Sequence:](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/uml-sequence.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/uml-sequence.png)

### 7. Описание состава [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Component) [✋](https://github.com/stankin/design-part-2/wiki/LR-7)

* **Описываемый объект:** Структура программных средств

* [Диаграмма UML Component:](https://github.com/ZhuravlevD/projectIS/blob/main/scr/uml-component.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr/uml-component.png)

### 8. Демонстрация реализации (личная страница)

* Личная страница на [Github](https://zhuravlevd.github.io/Zhuravlev-student-page/#!/topics)

### 9. Подготовка к интерпретации построенных моделей

**9.1 Используемые паттерны проектирования и разработки [✋](https://github.com/stankin/design-part-2/wiki/sem2):**

* **Процессная модель для сравнения:**
* Задача: необходимо повысить эффективность работы с данными о состояниях оборудования и пп
* Решение задачи при помощи методологии PDCA:
1.	Plan (Планирование) :<br>
1.1 Выявленные проблемы :<br>
* Тратится много времени на анализ данных о состояниях оборудования и п/п <br>
1.2 Цель: Оптимизировать временные затраты на анализ информации о состоянии оборудования и п/п <br>
1.3 Требования: Повысить эффективность без увеличения трудозатрат <br>
1.4 Ожидаемый результат: Повышение эффективности труда сотрудников <br>
1.5 Ресурсы, необходимые для достижения ожидаемого результата: сервер, БД, Web-сервер <br>
1.6 Процессы (запланированные действия): <br>
* Проектирование 
* Моделирование
* Разработка системы
* Тестирование

2.	Do (Выполнение) : <br>
Администратор и инженеры-технологи выполняют поставленные задачи

3.	Check (Проверка) : <br>
По итогу внедрения производится анализ результатов

4.	Act (Улучшение) : <br>
Если использование данной СУБД в работе повышает эффективность на производстве, то она берется на сопровождение с последующей доработкой

* **Используемые в разработке паттерны и фреймворки:**
Паттерн:  Model-View-Presenter

**9.2 Используемые паттерны выявления проблем [✋](https://github.com/stankin/design-part-2/wiki/sem3):**
Муда: Ручной сбор данных и анализ
Мура: Составление план-графика раз в месяц
Мури: Переутомление инженера-технолога

**9.3 Возможные антипаттерны [✋](https://github.com/stankin/design-part-2/wiki/sem4):**

| Категория  | Антипаттерн (риск) | Действие по избежанию |
|---|---|---|
| Разработка | Таинственный код (Cryptic code) - использование аббревиатур вместо мнемоничных имён | Давать переменным понятные названия, которые соответствуют их прямому назначению |
| Архитектура | Затычка на ввод данных (Input kludge): Забывчивость в спецификации и выполнении поддержки возможного неверного ввода. | Продумать алгоритм проверки пользовательского ввода. |
| Организация | Разработка комитетом (Design by committee): разработка проекта без централизованного управления или без компетентного руководства. | Разработать методику взаимодействия между командами. |
| Среда | Город ларьков (Kiosk City): каждый отдел вырабатывает свой собственный механизм обмена информацией | Ввести правило обязательного согласования всех механизмов обмена информацией с директором по цифровому развитию |

### 10. Интерпретация построенных моделей

**10.1 Определение числовых показателей для поставленной цели моделирования:**

Определение процессов требующих повышения качества

![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/Процессы.PNG)

Способ получения: извлечение из диаграмм IDEF0 и DFD.

**10.2 Определение числовых показателей для цели потенциального проекта автоматизации: [✋](https://github.com/stankin/design-1/wiki/interpret_process)**

Сотрудник, чтобы найти и проанализировать в служебных записках информацию о состоянии определенного оборудования или производственного процесса в конкретном цеху тратит в среднем 30 минут. Помимо этого, сотруднику необходимо сначала найти служебные записки нужного цеха, на что он в свою очередь тратит порядка 20 минут. В среднем на предприятии насчитывается около 15 цехов, 300 оборудования и около 2000 производственных процессов. Следовательно, для того чтобы проанализировать информацию о всём оборудовании и всех производственных процессах сотруднику потребуется примерно 774 часа, т.е. около 97 рабочих дней, при учете того, что рабочий день будет длиться 8 часов.

**10.3 Расчет потенциального эффекта от автоматизации:**

После создания БД для хранения и анализа данных о состоянии оборудования и производственных процессов сотрудник будет тратить на поиск нужного цеха около 30 секунд. После нахождения цеха сотрудник будет тратить около 1 минуты на поиск и анализ информации о состоянии оборудования и производственных процессов или же 2307,5 минут (38 часов) на поиск информации о всех оборудованиях и всех производственных процессах.
774ч-38ч=736 ч/год = 61 ч/месяц - экономия трудозатрат работника. 

**10.4 Определение числовых показателей и расчет трудозатрат на разработку программных средств:**

Расчет сложности разработки методом FPA IFPUG:

![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/fpa.PNG)

Расчет трудозатрат на разработку «с нуля» методом COCOMO II:

![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/cocomo.PNG)

**10.5 Сравнительный план-факт:**

Исходя из расчетов п. 10.4 можно сформировать следующую таблицу:

![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr1/план-факт1.PNG)

Из расчета:

* SLOC = 2 376 строк кода

* PM (Трудозатраты) = 10,5 человеко-месяцы

* TDEV (Полный срок разработки, месяцы) = 7,1 месяцев


Исходя из значений по факту:

* SLOC = 1300 строк кода

* PM (Трудозатраты) = 7,1 человеко-месяцы

* TDEV (Полный срок разработки) = 6 месяцев

* Готовность = 80%

**ВЫВОДЫ**

Исходя из результатов таблицы п.10.5 можно сделать вывод, что за счет использования готовых функций и библиотек удалось сократить строки кода (языки программирования C#) в 1,5 раза. Также, за счет сокращения тестирования, объема документации, и использования CASE, удалось сократить срок разработки с 7,1 месяцев до 6. Срок окупаемости разработки сократился в 1,2 раза. На данный момент работа выполнена на 80%, и на остаток реализации по расчету осталось около 15 часов.
