## Курсовой проект по дисциплине "Проектирование информационных систем"

## ФИО, ИДБ-17-06

### 1. Определение требований к модели [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

**Тема ВКР:** Разработка СУБД для хранения и анализа состояний оборудования и производственных процессов из различных отраслей машиностроительного производства

**Объект исследований:** современное машиностроительное производство

**Предмет исследований:** состояния оборудования и производственных процессов из различных отраслей машиностроительного производства

**Процессы верхнего уровня:** [✋](https://github.com/stankin/design-part-2/wiki/sem1)
* **А1** Создание БД состояний оборудования и производственных процессов
* **А2** Сбор данных о состояниях оборудования и производственных процессов
* **А3** Систематизация и анализ данных о состояниях оборудования и производственных процессов
* **А4** Запись данных о состояниях оборудования и производственных процессов


**Точка зрения:** Инженер-технолог

**Цель моделирования:** Определение автоматизируемых функций

### 2. Функциональное моделирование процессов (IDEF0) [✋](https://github.com/stankin/design-part-2/wiki/LR-1)

* A-0 

![A-0](https://github.com/ZhuravlevD/projectIS/blob/main/scr/A0.PNG)

* A0 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr/1A0.PNG)

* Декомпозиция A1 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr/A1.PNG)

* Декомпозиция A2 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr/A2.PNG)

* Декомпозиция A3 

![A0](https://github.com/ZhuravlevD/projectIS/blob/main/scr/A3.PNG)

### 3. Функциональное моделирование программных и информационных средств (DFD) [✋](https://github.com/stankin/design-part-2/wiki/LR-2)

**Конфигурация технических средств:** Сервер хранения данных

**Конфигурация программных средств:** Многоуровневая

**Допустимые виды хранилищ и их размещение:** <файлы, директории, репозитории, базы данных>

* A32 Автоматизация процесса А32

![32](https://github.com/ZhuravlevD/projectIS/blob/main/scr/А32.PNG)

* A33 Автоматизация процесса А33

![A33](https://github.com/ZhuravlevD/projectIS/blob/main/scr/А33.PNG)

* A4 Автоматизация процесса А4

![A4](https://github.com/ZhuravlevD/projectIS/blob/main/scr/A4.PNG)

### 4. Описание выбранного процесса [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате прецедента (Use Case) [✋](https://github.com/stankin/design-part-2/wiki/LR-4)

* [Диаграмма UML Use Case:](https://github.com/ZhuravlevD/projectIS/blob/main/scr/usecase.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr/usecase.png)

**4.1 Идентификатор прецедента:** A2

**4.2 Название прецедента:** Сбор данных

**4.3 Контекст:** A0 СУБД для хранения и анализа состояний оборудования и производственных процессов из различных отраслей машиностроительного производства

**4.4 Участники (actors) и цели (goals):**

| Участник  | Категория  | Цель (goal) |
|---|---|---|
|Начальник цеха | внешний  | организация сбора данных |
| Инженер-технолог | основной  | осуществление сбора данных |

**4.5 Предусловия (pre-conditions):**
* Начальник цеха определил необходимое оборудование и производственные процессы
* Инженер-технолог и может начать работу с оборудованием и производственными процессами
**4.6 Постусловия (post-conditions):**

* Ненормализованные данные о состояниях оборудования и производственных процессов

**4.7 Основной поток выполнения (main flow)**:

| Участник  | Действие (activity)  | Ожидаемый результат |
|---|---|---|
| Инженер-технолог | начало работы с оборудованием и производственными процессами | исправное оборудование и отсутствие ошибок в пп |
| Инженер-технолог | составление плана выборки | готовый план |
| Инженер-технолог | выбор метода сбора данных | выбранный метод |
| Инженер-технолог | подготовка к сбору информации | анкета для сбора |
| Инженер-технолог | проведение сбора | ненормализованные данные о состояниях оборудования и производственных процессов |

**4.8 Исключения (exceptions):**

| Условие (риск) | Последствия | Реакция |
|---|---|---|
| Отсутствие необходимого оборудования/пп в плане выборки | невозможность фиксации данных о состоянии оборудования/пп | пересмотр плана |
| Полностью неисправное оборудование | невозможность фиксации данных о его состоянии | отправка на принудительный ремонт  |

**4.9 Альтернативы (alternates):**

| Участник  | Действие (activity)  | Ожидаемый результат |
|---|---|---|
| Техник | проведение техосмотра оборудования | отсутствие неисправностей |

**4.10 Временные параметры:**

* **Триггер (событие, стартующее прецедент):** Получение оборудования/пп

* **Номинальная частота повторения прецедента:** 1 раз в месяц

* **Продолжительность прецедента:** 20 часов

### 5. Описание структуры объекта [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате ERD (Class) [✋](https://github.com/stankin/design-part-2/wiki/LR-5)

* **Описываемый объект:** описание ролей, модулей приложения для работы с БД для хранения и анализа данных о состоянии оборудования и производственных процессов

* [ER-диаграмма ролей](https://github.com/ZhuravlevD/projectIS/blob/main/scr/Er-role.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr/Er-role.png)
* [ER-диаграмма модулей](https://github.com/ZhuravlevD/projectIS/blob/main/scr/Er-mod.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr/Er-mod.png)

### 6. Описание алгоритма [✋](https://github.com/stankin/design-part-2/wiki/LR-3) в формате UML (Sequence) [✋](https://github.com/stankin/design-part-2/wiki/LR-6)

* **Описываемые процессы и потоки данных:** Создание БД, обработка и анализ данных, проверка корректности данных, заполнение БД, Отоброжание данных в приложении
* [Диаграмма UML Sequence:](https://github.com/ZhuravlevD/projectIS/blob/main/scr/uml-sequence.txt):
![p5](https://github.com/ZhuravlevD/projectIS/blob/main/scr/uml-sequence.png)

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
1.	Plan (Планирование) :
1.1 Выявленные проблемы :
Тратится много времени на анализ данных о состояниях оборудования и пп
Тратится много времени на поиск информации о состояниях оборудования и пп
1.2 Цель: Оптимизировать временные затраты на поиск информации о состояниях оборудования и пп
1.3 Требования: Повысить эффективность без увеличения трудозатрат
1.4 Ожидаемый результат: Повышение эффективности труда сотрудников
1.5 Ресурсы, необходимые для достижения ожидаемого результата: сервер, БД, Web-сервер
1.6 Процессы (запланированные действия):
Проектирование структуры метаданных
Разработка БД для хранения и анализа данных о состояниях оборудования и пп
Внедрение БД для хранения и анализа данных о состояниях оборудования и пп
2.	Do (Выполнение) : 
Администратор и инженеры-технологи выполняют поставленные задачи
3.	Check (Проверка) : 
По итогу внедрения производится анализ результатов
4.	Act (Улучшение) : 
Если использование данной БД в работе повышает эффективность на производстве, то она берется на сопровождение с последующей доработкой

* **Используемые в разработке паттерны и фреймворки:**
Паттерн:  Model-View-Presenter

**9.2 Используемые паттерны выявления проблем [✋](https://github.com/stankin/design-part-2/wiki/sem3):**
* Муда: Организация разработки БД
* Мура: Внесение изменений в ТЗ под конец разработки
* Мури: Перегрузка серверов БД из-за огромного количества информации

**9.3 Возможные антипаттерны [✋](https://github.com/stankin/design-part-2/wiki/sem4):**

| Категория  | Антипаттерн (риск) | Действие по избежанию |
|---|---|---|
| Разработка | Таинственный код (Cryptic code) - использование аббревиатур вместо мнемоничных имён | Давать переменным понятные названия, которые соответствуют их прямому назначению |
| Архитектура | Затычка на ввод данных (Input kludge): Забывчивость в спецификации и выполнении поддержки возможного неверного ввода. | Продумать алгоритм проверки пользовательского ввода. |
| Организация | Разработка комитетом (Design by committee): разработка проекта без централизованного управления или без компетентного руководства. | Разработать методику взаимодействия между командами. |
| Среда | Город ларьков (Kiosk City): каждый отдел вырабатывает свой собственный механизм обмена информацией | Ввести правило обязательного согласования всех механизмов обмена информацией с директором по цифровому развитию |

### 10. Интерпретация построенных моделей

**10.1 Определение числовых показателей для поставленной цели моделирования:**

**10.2 Определение числовых показателей для цели потенциального проекта автоматизации: [✋](https://github.com/stankin/design-1/wiki/interpret_process)**

**10.3 Расчет потенциального эффекта от автоматизации:**

**10.4 Определение числовых показателей и расчет трудозатрат на разработку программных средств:**

**ВЫВОДЫ**

