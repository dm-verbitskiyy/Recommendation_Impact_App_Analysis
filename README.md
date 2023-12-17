# Recommendation Impact App Analysis
## Анализ влияния новой системы рекомендаций на эффективность приложения по доставке продуктов

Исследование выполнено с использованием Jupyter Notebook на языке программирования Python. В процессе анализа данных применялись следующие библиотеки: pandas, scipy.stats (ttest_ind).

--- 

### Задачи для Анализа:

1) Загрузить данные о заказах пользователей в приложении по доставке продуктов.

2) Объединить данные из таблиц заказов, данных пользователей и информации о продуктах.

3) Оценить эффективность новой системы рекомендаций приложения, проведя АБ-тест с двумя группами пользователей: группа 0 (старая версия приложения) и группа 1 (новая система рекомендаций).

### Описание данных:

ab_users_data: содержит информацию о пользователях, историю заказов и действия пользователей в приложении. 

 - Колонки: user_id, order_id, action, time, date, group.

ab_orders: предоставляет подробную информацию о составе заказов. 

 - Колонки: order_id, creation_time, product_ids.

ab_products: содержит подробную информацию о продуктах. 

 - Колонки: product_id, name, price.

---

### Выводы по Исследованию:

1) Средняя сумма заказа для группы 0 составляет 400.2, а для группы 1 - 390.22. Проведенный t-тест не выявил статистически значимых различий в средних чеках между группами (p-значение = 0.2591). Следовательно, новая система рекомендаций не оказывает влияния на средний чек.

2) Среднее количество заказов на пользователя для группы 0 составляет 11, а для группы 1 - 18. Проведенный t-тест показал статистически значимые различия (p-значение < 0.05), что говорит о влиянии новой системы рекомендаций на увеличение количества заказов.

3) Общая выручка для группы 0 составляет 643521.7, а для группы 1 - 979835.6. Однако, статистический тест не выявил значимых различий в общей выручке между группами (p-значение = 0.0835). Следовательно, новая система рекомендаций не оказывает статистически значимого влияния на общую выручку.

### Общий Вывод:

На основе проведенного анализа, можно рекомендовать включить новую систему рекомендаций на всех пользователей приложения, так как она положительно влияет на количество заказов на пользователя без негативного воздействия на средний чек или общую выручку.
