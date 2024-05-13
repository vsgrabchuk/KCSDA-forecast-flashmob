# KCSDA-forecast-flashmob

## Преамбула
Социальная сеть. Команда маркетологов решила организовать флэшмоб в ленте новостей: участники должны сделать пост, где они рассказывают какой-то интересный факт о себе, и опубликовать его с хэштегом. Три поста, собравших наибольшее число лайков, получают призы.

Флэшмоб проходил с 2024-03-15 по 2024-03-21. 

## Задача
Оценить эффективность флэшмоба

## План:
1) Определить целевые метрики, которые могли измениться во время флэшмоба
2) Повлиял ли влешмоб на метрики и насколько?
3) Имел ли флэшмоб долгосрочные эффекты?

## Решение
1) Используемые метрики:
- DAU
- views, mean_views(на пользователя)
- likes, mean_likes(на пользователя)
- количество постов
- CTR
2) Оценка влияния происходит с помощью causal inference (предсказание временного ряда без оказания влияния и сравнение с реальными данными):
- DAU
  - нестатзначимый эффект 
- views
  - положительный статзначимый эффект (увеличение в ~2 раза)
- mean_views(на пользователя)
  - положительный статзначимый эффект (увеличение в ~2 раза)
- likes
  - положительный статзначимый эффект (увеличение в ~2 раза)
- mean_likes(на пользователя)
  - положительный статзначимый эффект (увеличение в ~2 раза)
- количество постов
  - положительный статзначимый эффект (увеличение на ~40 %)
- CTR
  - эффект принимается нестатзначимым
- retention
  - нестатзначимый эффект
3) Оценка долгосрочного эффекта происходит с помощью causal inference
  - флешмоб не оказал влияния в долгосрочной перспективе

## Stack
- python
  - pandas
  - numpy
  - pandahouse
  - tensorflow
  - tensorflow_probability
  - causalimpact
  - seaborn
  - matplotlib

## Идеи для улучшения
Модели имеют статическую ошибку в силу наличия положительного тренда в данных, необходимо учесть его вручную
