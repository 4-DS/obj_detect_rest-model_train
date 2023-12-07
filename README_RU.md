# Step CV-Pipeline: model_train [EN](README.md)

Данная компонент CV-Pipeline предназначен для конфигрурирования тренировки модели, загрузка predtraining весов и запуск обучения модели

Входные данные для step CV-Pipeline: model_train
- **coco_train_dataset**     
Тренировочный датасет
- **coco_eval_dataset**     
Валидационный датасет
- **yolox_pth_pretrain_weights**     
Predtraining веса модели

Выходом работы данного step CV-Pipeline является
- **obj_detect_inference_files**     
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
