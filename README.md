# Анализ датасета «Medical Cost Personal Datasets»
Датасет доступен по ссылке: https://www.kaggle.com/datasets/mirichoi0218/insurance.
Он содержит данные о медицинских расходах, покрываемых страховкой, среди жителей США. Помимо расходов, приведена информация о возрасте; поле; индексе массы тела (ИМТ), нормой которого считается ИМТ от 18.5 до 24.9; количестве детей; о том, курит человек или нет, и территории проживания в США.
В анализе я остановилась на двух параметрах, от которых может зависеть размер медицинских расходов: курении и ИМТ.
## Задачи:
1. Выяснить, различаются ли медицинские расходы у курящих и некурящих людей
2. Проверить, есть ли связь между курением и полом человека
3. Проверить, есть ли корреляция между медицинскими расходами и ИМТ
4. Построить 95% доверительный интервал для ИМТ
## Результаты:
### 1. Зависимость медицинских расходов от курения
Для анализа использовался тест Манна-Уитни, так как медицинские расходы не имеют нормального распределения, полученное значение p-value = 2.6×10-130.
Значение p-value говорит о том, что на любом разумном уровне значимости мы можем утверждать, что медицинские расходы курящих людей действительно выше, чем некурящих.
### 2. Зависимость курения от пола
Использовался тест χ2 на независимость, полученное значение p-value = 0.0065.
Получили, что на 5% уровне значимости достаточно оснований, чтобы отвергнуть гипотезу о независимости.
### 3. Зависимость медицинских расходов от ИМТ
Для выявления зависимости была построена модель линейной регрессии для медицинских расходов и ИМТ в двух группах: курящих и некурящих людей – и рассчитан коэффициент корреляции Пирсона.
Для курящих:
r = 0.806
p-value = 5.02×10-64
Для некурящих:
r = 0.084 p-value = 0.006
На 5% уровне значимости можно утверждать, что медицинские расходы скоррелированы с ИМТ в обеих группах. Однако у некурящих людей коэффициент корреляции близок к нулю, а R2 = 0.007. Это означает, что дисперсия значений медицинских расходов всего лишь на 0.7% объясняется зависимостью от ИМТ.
### 4. Доверительный интервал для индекса массы тела
Построим 95% доверительный интервал для ИМТ.
Средний ИМТ: 30.66
Доверительный интервал: (30.33, 30.99)
Интересно, что данные значения выше нормы и соответствуют ожирению первой степени.
## Выводы:
 1. Медицинские расходы курящих людей достоверно выше, чем у некурящих
2. Наблюдается зависимость между курением и гендером человека
3. Присутствует корреляция между медицинскими расходами и индексом массы тела
и у курящих, и у некурящих людей
4. 95% доверительный интервал для среднего индекса массы тела - (30.33, 30.99)
