# Step CV-Pipeline: model_train [EN](README.md)

Данная компонент CV-Pipeline предназначен для конфигрурирования тренировки модели, загрузка predtraining весов и запуск обучения модели

Создается на основе [шаблона](https://github.com/4-DS/step_template).
Чтобы не забывать про обязательные ячейки в каждом ноутбуке, проще всего создавать новые ноутбуки просто копированием [`substep_full.ipynb`](https://github.com/4-DS/step_template/blob/main/substep_full.ipynb) из стандартного [шаблона](https://github.com/4-DS/step_template) компоненты.

Входные данные для step CV-Pipeline: model_train
- **train_data**     
Тренировочный датасет изображений, сохраненный в parquets

- **eval_data**     
Валидационный датасет изображений, сохраненный в parquets

- **train_eval_config**     
Аннотациии тренировочного и валидационного датасета изображения

Конечным выходом работы данного step CV-Pipeline является
- **model**     
Сохраненные веса обученной модели (веса последней эпохи и с лучшими достигнутыми метриками), конфигурационные файлы

## Как запустить шаг CV-Pipeline: model_train

### Создать директорию для проекта (или использовать уже существующую)
```
mkdir obj_detect_binary
cd obj_detect_binary
```  

### склонировать репозиторий model_train
```
git clone --recurse-submodules https://github.com/4-DS/obj_detect_binary-model_train.git {dir_for_model_train}
cd {dir_for_model_train}
```  

### запустить шаг CV-Pipeline:model_train
```
python step.dev.py
```  
или
```
step.prod.py
``` 
