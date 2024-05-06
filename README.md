# ML-in-chem
##Linear Regression
1) Из CSV-файла загружаем датасет с информацией о химических соединениях в виде SMILES.
2) Для каждого SMILES создается объект молекулы RDKit
2.1) Для каждой молекулы извлекаются химические характеристики в виде MACCS ключей и вычисляется логарифмическое распределение коэффициентов разделения.
3) Создаем матрицы признаков X (MACCS) и y(LogP) - таргет-величину
4) Модель градиентного спуска
4.1) Задаем первоначальные веса и смещения. Необходимо определить такие w*, b*, чтобы зависимость 
y = w1x1+w2x2+...+b максимально приближала Loss к 0.
4.2) Определяем функцию потерь
4.3) Определяем градиенты по отношению к весам и смещению (dl/dw = 0, dl/db = 0)
4.4) Осуществляем обучение модели таким образом, чтобы при каждой итерации обновление весов происходило в противоположном направлении градиенту.
4.5) Процесс происходит до минимизации значительных изменений в функции потерь
4.6) Визуализация показала уменьшение GD. ТРЕБУЕТСЯ доработка в отношении соотношения размерностей матриц.
