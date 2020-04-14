Модель нейронной сети прошла 4 этапа обучения по 60 эпох:

* Исходная сеть с двумя Conv2D слоями с kernel_size = 3, двумя MaxPool2D, одним flatten и одним dense с активацией softmax. (**Оранжевый цвет на графиках**)
* Добавил свёрточный слой и повторил процесс обучения. Итого: 3 Conv2D слоя с kernel_size = 3, 3 MaxPool2D, 1 flatten и 1 dense с активацией softmax. (**Синий цвет на графиках**)
* Изменил кол-во свёрток (kernel_size) в свёрточном слое и повторил процесс обучения. Итого: 1 Conv2D слой с kernel_size = 1, 1 Conv2D с kernel_size = 2, 1 Conv2D c kernel_size = 3, 3 MaxPool2D, 1 flatten и 1 dense с активацией softmax. (**Красный цвет на графиках**)
* Добавил четвёртый свёрточный слой и изменил кол-во свёрток в свёрточных слоях. Итого: 2 Conv2D с
 kernel_size = 1, 1 Conv2D с kernel_size = 2, 1 Conv2D с kernel_size = 3, 4 MaxPool2D, 1 flatten и 1 dense с активацией softmax. (**Голубой цвет на графиках**)

 На всех 4-х этапах при обучении сети использовались: 
 * Оптимизатор 'sgd'
 * Функция 'потерь categorical_crossentropy'
 * Метрика 'categorical_accuracy'
 
 BATCH_SIZE = 55

 Графики метрики точности и функции потерь на обучающей выборке:

 ![Train accuracy](https://i.ibb.co/cDG8CJK/image.png)
 ![Train losses](https://i.ibb.co/QH10XPf/image.png)

 Графики метрики точности и функции потерь на валидационной выборке:

 ![Validation accuracy](https://i.ibb.co/JzCwfvv/image.png)
 ![Validation losses](https://i.ibb.co/QdrK7RB/image.png)