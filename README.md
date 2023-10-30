![interface model_train_interface.drawio](./imgs/model_train_interface.drawio.png)

# Step CV-Pipeline: model_train

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

## How to run CV-Pipeline step

### create directory for project
```
mkdir yolox_mmdet
cd yolox_mmdet
```  

### clone repository 
```
git clone --recurse-submodules https://gitlab.com/yolox_mmdet/model_train.git {model_train}
cd model_train
```  

### run step
```
python step.dev.py
```  
or
```
step.prod.py
``` 
