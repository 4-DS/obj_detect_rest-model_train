![interface model_train_interface.drawio](./imgs/model_train_interface.drawio.png)

# Step CV-Pipeline: model_train [RU](README_RU.md)

This CV-Pipeline component is intended for configuring model training, loading predtraining weights and starting model training

Created based on [template](https://github.com/4-DS/step_template).
In order not to forget about the required cells in each laptop, the easiest way to create new jupyter notebooks is simply by copying [`substep_full.ipynb`](https://github.com/4-DS/step_template/blob/main/substep_full.ipynb) from standard [template](https://github.com/4-DS/step_template).

Input data for step CV-Pipeline: model_train
- **train_data**     
Training image dataset saved by parquets

- **eval_data**     
Validation dataset of images saved by parquets

- **train_eval_config**     
Annotations and training and validation image dataset

The final output of this step CV-Pipeline is
- **model**     

Saved weights of the trained model (weights of the last epoch and with the best achieved metrics), configuration files

## How to run a step CV-Pipeline: model_train

### Create a directory for the project (or use an existing one)
```
mkdir yolox_mmdet
cd yolox_mmdet
```  

### clone the repository: model_train
```
git clone --recurse-submodules https://gitlab.com/yolox_mmdet/model_train.git {model_train}
cd model_train
```  

### run step CV-Pipeline:model_train
```
python step.dev.py
```  
or
```
step.prod.py
``` 
