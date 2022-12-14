# Очистка руды

## Описание проекта
Имеются данные с параметрами добычи и очистки. Необходимо построить модель, которая будет предсказать коэффициент восстановления золота из золотосодержащей руды. Она поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.
### Статус проекта
Завершен ✅
### Результат проекта
Найдены параметры концентрации металлов на разных этапах очистки, изучено распределения размеров гранул сырья на обучающей и тестовой выборках, исследована суммарная концентрация всех веществ на разных стадиях: в сырье, в черновом и финальном концентратах. Обучены DecisionTreeRegressor, LinearRegression и RandomForestRegressor с метрикой SMAPE.

## Описание данных
### Технологический процесс
- ```Rougher feed — ис```ходное сырье
- ```Rougher additions (или reagent additions)``` — флотационные реагенты: Xanthate, Sulphate, Depressant
- ```Rougher process (англ. «грубый процесс»)``` — флотация
- ```Rougher tails``` — отвальные хвосты
- ```Float banks``` — флотационная установка
- ```Cleaner process``` — очистка
- ```Rougher Au``` — черновой концентрат золота
- ```Final Au``` — финальный концентрат золота
### Параметры этапов
- ```air amount``` — объём воздуха
- ```fluid levels``` — уровень жидкости
- ```feed size``` — размер гранул сырья
- ```feed rate``` — скорость подачи
### Наименование признаков
#### Наименование признаков должно быть такое:
```[этап].[тип_параметра].[название_параметра]```
#### Возможные значения для блока ```[этап]```:
- ```rougher``` — флотация
- ```primary_cleaner``` — первичная очистка
- ```secondary_cleaner``` — вторичная очистка
- ```final``` — финальные характеристики
#### Возможные значения для блока ```[тип_параметра]```:
- ```input``` — параметры сырья
- ```output``` — параметры продукта
- ```state``` — параметры, характеризующие текущее состояние этапа
- ```calculation``` — расчётные характеристики

## Библиотеки
- ```pandas```
- ```numpy```
- ```sklearn```
- ```matplotlib```
- ```seaborn```
