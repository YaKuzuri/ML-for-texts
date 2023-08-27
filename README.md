# ML for texts
Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 

Требуется обучить модель классифицировать комментарии на позитивные и негативные. В нашем распоряжении набор данных с разметкой о токсичности правок. Значением метрики качества *F1* должно быть не меньше 0.75. 

Данные находятся в файле `toxic_comments.csv`. Столбец *text* в нём содержит текст комментария, а *toxic* — целевой признак.
# Skills and tools
- pandas
- nltk
- sklearn.feature_extraction.text.TfidfVectorizer
- sklearn.model_selection.GridSearchCV
- sklearn.pipeline.Pipeline
- numpy
- re
- tqdm

- sklearn.linear_model.LogisticRegression
- sklearn.dummy.DummyClassifier
- sklearn.ensemble.RandomForestClassifier
- lightgbm.LGBMClassifier
- catboost.CatBoostClassifier

# Сonclusions
Удалось добится значения F1 почти в 0.777 используя логистическую регрессию, что соответствует требованиям заказчика (F1 > 0.75).
