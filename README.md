# deep_learning_3_task
Бинарная классификация отзывов о мобильных телефонах на положительные и отрицательные.

# Данные
Данные взяты отсюда: https://www.kaggle.com/datasets/theovall/phonereviews
В репозитории нет файла с данными, так как из-за его больших размеров gethub не дал его загрузить.

# Принцип классификации
В работе использовалась TF-IDF векторизация отзывов.
Для формирования целевой переменной (target) в датасете послужило поле rating. Переменная target формировалась следующим образом: Если rating >= 4, считаем
отзыв положительным (target = 1), если же rating < 4, то отрицательным (target = 0). 

# Модели
В работе использовались две модели машинного обучения: логистическеая регрессия, и Random Forest с тюнингом параметров.


# Метрики
В качестве интересующих нас метрик были выбраны accuracy и F-мера (гармоническое среднее между Precision и Recall). Это обусловлено тем, что для данной
задачи плохо, как распознавать отзывы ложно положительно, так и ложно отрицательно.

### Для логистричкокй регрессии значение метрик:
F-мера: 0.8781793842034805
Accuracy: 0.818

### Для Random Forest значение метрик:
F-мера: 0.8590785907859079
Accuracy: 0.792
