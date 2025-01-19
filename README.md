Проведено дообучение модели "small" от OpenAI Whisper для русского языка на датасете Sber-golos.
Исходная предобученная модель взята с GitHub: https://github.com/openai/whisper
Обучение проводилось на данных из статьи https://habr.com/ru/company/sberdevices/blog/559496/
Данные для обучения были взяты с GitHub: https://github.com/sberdevices/golos?tab=readme-ov-file

Дообучение проведено на данных из train_crowd0.tar - 11 GB, что составляет 10% от общего количества данных. 
Обучение длилось 1522 минуты - 16,42 эпохи. Лучшее значение WER - 22.899838% (на 5% от полного размера теста - test.tar - 1.3 GB) было получено на шаге - 5300 - 6,8 эпохи. Для сравнения, тест на тех же данных модели "small" от OpenAI Whisper дает точность WER=62,96%
Дообученая модель на 100% размера теста - test.tar - 1.3 GB дает точность около WER = 26%.

Ноутбук my_whisper.ipynb с кодом доступен для скачивания по ссылке - https://disk.yandex.ru/d/k2H0gaLWm1uB5A
Логи обучения tensorboard runs.zip доступены для скачивания по ссылке - https://disk.yandex.ru/d/Ll-9QdJejKfgcw
Для продолжения обучения модели лучший чекпоинт в архиве checkpoint-6300.zip можно скачать по ссылке - https://disk.yandex.ru/d/BVQlOYwQF6o8Dg
Сохраненную модель в архиве docker.zip с возможностью  развертывания веб-приложения с использованием Docker можно скачать по ссылке - https://disk.yandex.ru/d/6y-0dg-vg752Fw
Одной из целей данного проекта было найти оптимальные гиперпараметры для обучения модели "small" от OpenAI Whisper и получение наилучшего значения WER в условиях меньшего датасета. 
В связи особенность датасета Sber-golos дообучение модель утратила способность расставлять пунктуацию.
Ноутбуке my_whisper.ipynb доступен для скацивания на GitHub.


The "small" model from OpenAI Whisper for the Russian language was retrained on the Sber-golos dataset.
The original pre-trained model was taken from GitHub: https://github.com/openai/whisper
Training was carried out on data from the article https://habr.com/ru/company/sberdevices/blog/559496/
Training data was taken from GitHub: https://github.com/sberdevices/golos?tab=readme-ov-file

Retraining was carried out on data from train_crowd0.tar - 11 GB, which is 10% of the total data.
Training lasted 1522 minutes - 16.42 epochs. The best WER value - 22.899838% (on 5% of the full test size - test.tar - 1.3 GB) was obtained at step - 5300 - 6.8 epochs. For comparison, a test on the same data of the "small" model from OpenAI Whisper gives an accuracy of WER = 62.96%
The retrained model on 100% of the test size - test.tar - 1.3 GB gives an accuracy of about WER = 26%.

The my_whisper.ipynb notebook with the code is available for download at the link - https://disk.yandex.ru/d/k2H0gaLWm1uB5A
Tensorboard runs.zip training logs are available for download at the link - https://disk.yandex.ru/d/Ll-9QdJejKfgcw
To continue training the model, the best checkpoint in the checkpoint-6300.zip archive can be downloaded at the link - https://disk.yandex.ru/d/BVQlOYwQF6o8Dg
The saved model in the docker.zip archive with the ability to deploy a web application using Docker can be downloaded at the link - https://disk.yandex.ru/d/6y-0dg-vg752Fw
One of the goals of this project was to find the optimal hyperparameters for training the "small" model from OpenAI Whisper and obtain the best WER value under conditions of lower dataset.
Due to the peculiarity of the Sber-golos dataset, the model lost the ability to place punctuation after additional training.
The my_whisper.ipynb notebook is available for download on GitHub.