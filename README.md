# NER-in-medieval-German-texts

В этом репозитории находятся все материалы для диплома по теме "Распознавание именованных сущностей в средневековых немецких текстах".

В файле [PDFtoText] (https://github.com/Maryleya/NER-in-medieval-German-texts/blob/main/PDFtoText.ipynb) находится код для распознавания текста в PDF формате, перевода его в обычный текстовый формат и последующей очистки текста. Используя этот код, был собран корпус из 7 средневековых немецких текстов - Alpharts Tod, Dietrich und Wenezlan, Dietrichs Flucht, Nibelungenlied, Rabenschlacht, Rosengarten, и Wunderer. Кроме того, в нем можно увидеть статистику по собранному корпусу - число предложений, число словоупотреблений и процент словоупотреблений.

В файле [Dataset] (https://github.com/Maryleya/NER-in-medieval-German-texts/blob/main/Dataset.csv) находится датасет, состоящий из именованных сущностей собранного корпуса с тегами PERSON, REGION, CITY, WATER, GROUP и PROPERTY.

В файле [NER] (https://github.com/Maryleya/NER-in-medieval-German-texts/blob/main/NER.ipynb) находится код обучения моделей. Сначала приведена BIO-разметка текста Nibelungenlied на основе датасета (Besnier, Mattingly 2021), далее текст разбивается на train, validation и test и идет обучение на этом тексте трех моделей - Distilroberta-base-mhg-charter-mlm, GHisBERT и SequenceTagger от Flair. Все обученные модели хранятся в [гугл-папке] (https://drive.google.com/drive/folders/10F22FqiX2g_0mOdnr_Y5ZstGk0teRXpU?usp=sharing).

В файле [Test_on_Dietrich] (https://github.com/Maryleya/NER-in-medieval-German-texts/blob/main/Test_on_Dietrich.ipynb) находится код по тестированию обученных моделей. Сначала приведена BIO-разметка 6 текстов о Дитрихе на основе собранного датасета, затем обученные модели оцениваются на данных текстах. Для каждой модели строится classification report (отчет о классификации) и confusion matrix (матрица ошибок), а также указана метрика accuracy (аккуратность).
