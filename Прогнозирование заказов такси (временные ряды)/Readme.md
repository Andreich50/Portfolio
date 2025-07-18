#  Прогнозирование заказов такси
Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час. Постройте модель для такого предсказания.

Значение метрики *RMSE* на тестовой выборке должно быть не больше 48.

Вам нужно:

1. Загрузить данные и выполнить их ресемплирование по одному часу.
2. Проанализировать данные.
3. Обучить разные модели с различными гиперпараметрами. Сделать тестовую выборку размером 10% от исходных данных.
4. Проверить данные на тестовой выборке и сделать выводы.


Данные лежат в файле `taxi.csv`. Количество заказов находится в столбце `num_orders` (от англ. *number of orders*, «число заказов»).

**Цель:**

Предсказывать количество заказов на час вперед для определения потребности необъодимого количества водителей. 

**Задача:**

Основное задачей проекта является подбор модели для предсказания.

**Проект состоит из следующих этапов:**
1. Подготовка данных.
2. Анализ.
3. Обучение.
4. Тестирование.

## Выводы.

В данной работе были выполнены следующие этапы:
1. Проведена загрузка данных о количестве заказов такси из 26 тыс. значений с шагом 10 мин. Ресемплировано на один час.
2. Исследовательский анализ. Построены графики и выявлен тренд на возрастание количества заказов.
3. Для решения задачи регрессии построены три модели: одна линейная и две модели градиентного бустинга: CatBoost и LightGBM.
4. Методом кросс валидации проведена оценка работы моделей. Лучшей моделью по метрике RMSE выбрана CatBoost. Значение метрики составило 41.73 - соответствует условию.

**Рекомендация Заказчику:**

Для выполнения задачи предсказания количества заказов рекомендуется использовать обученную в данном проекте модель CatBoost.

