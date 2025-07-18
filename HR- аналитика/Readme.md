# HR аналитика компании "Работа с заботой"
# Описание проекта.
HR-аналитики компании «Работа с заботой» помогают бизнесу оптимизировать управление персоналом: бизнес предоставляет данные, а аналитики предлагают, как избежать финансовых потерь и оттока сотрудников. \
В этом HR-аналитикам пригодится машинное обучение, с помощью которого получится быстрее и точнее отвечать на вопросы бизнеса.


Компания предоставила данные с характеристиками сотрудников компании. Среди них:
— уровень удовлетворённости сотрудника работой в компании. Эту информацию получили из форм обратной связи: сотрудники заполняют тест-опросник, и по его результатам рассчитывается доля их удовлетворённости от 0 до 1, где 0 — совершенно неудовлетворён, 1 — полностью удовлетворён. \
Собирать данные такими опросниками не так легко: компания большая, и всех сотрудников надо сначала оповестить об опросе, а затем проследить, что все его прошли. 

# Задачи проекта.

1. **Регрессия**. Построить модель, которая сможет предсказать уровень удовлетворённости сотрудника на основе данных заказчика. 


Почему бизнесу это важно: удовлетворённость работой напрямую влияет на отток сотрудников. А предсказание оттока — одна из важнейших задач HR-аналитиков. Внезапные увольнения несут в себе риски для компании, особенно если уходит важный сотрудник.


2. **Классификация** Построить модель, которая сможет на основе данных заказчика предсказать то, что сотрудник уволится из компании.

**РЕЗУЛЬТАТ ВЫПОЛНЕНИЯ ЗАДАЧИ 1:**
1. С помощью рандомного поиска RandomizedSearch подбором гиперпараметров двух моделей и методов кодирования, масштабирования выбрана модель 
    
    **Дерева решений.**, со следующими гиперпараметрами: 
        - (max_depth=16, max_features=12, min_samples_split=13,random_state=42))])
2. На тестовой выборке метрика лучшей модели показала - **13.65**

**РЕЗУЛЬТАТ ВЫПОЛНЕНИЯ ЗАДАЧИ 2:**
1. С помощью рандомного поиска RandomizedSearch подбором гиперпараметров двух моделей и методов кодирования, масштабирования выбрана модель 
    
    **Дерева решений.**, со следующими гиперпараметрами: 
            - max_depth=5, max_features=6, random_state=42).
2. На тестовой выборке метрика лучшей модели показала - **0.91** 


3. Альтернативные модели показали худший результат.

**Рекомендации заказчику:**

1. Текучка кадров происходит у работников, которые работают меньше года и больше всего среди Junior специалистов.

2. Уровень удовлетворенности влияет на решение сотрудника об увольнении. Компании нужно уделить внимание на повышение уровня удовлетворенности: повысить зарплаты и уменьшать загруженность. Также влияет на решение об увольнение факты повышения сотрудников. Исходя из графиков, в категории кого повысили в прошлом году не имеется ни одного уволившегося.
