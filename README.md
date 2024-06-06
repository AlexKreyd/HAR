# HAR
Данная работа посвящена распознаванию человеческой активности (HAR) по данным с датчиков телефона.

Датасет: [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones)

Необходимо предсказть одну из следующих активностей:
- WALKING
- WALKING_UPSTAIRS
- WALKING_DOWNSTAIRS
- SITTING
- STANDING
- LAYING

Вначале были применены модели классического машинного обучения (K-ближайших соседей, логистическая регрессия, случайный лес, метод опорных векторов). Оптимальные значения гиперпараметров для этих моделей подбирались с помощью кросс-валидации.

Полученные значения accuracy на тестовой выборки:
- K-ближайших соседей - 0.891
- Логистическая регрессия - 0.961
- Случайный лес - 0.928
- Метод опорных векторов - 0.958

Также были использованы следующие нейронные сети: 1) CNN, LSTM, CNN + LSTM
1) CNN со следующей архитектурой:

![Image alt](https://github.com/AlexKreyd/HAR/blob/main/images/CNN.png)

Accuracy на тестовых данных: 0.945

2) LSTM со следующей архитекутрой:

![Image alt](https://github.com/AlexKreyd/HAR/blob/main/images/LSTM.png)

Accuracy на тестовых данных: 0.854

3) CNN + LSTM со следующей архитектурой:

![Image alt](https://github.com/AlexKreyd/HAR/blob/main/images/CNN_LSTM.png)

Accuracy на тестовых данных: 0.906

Также в ноутбуке представлены графики зависисмостей accuracy на train и validation подвыборках от количества эпох, а также матрицы ошибок (confusion matrix) для каждой модели.
