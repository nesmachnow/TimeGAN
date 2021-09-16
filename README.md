# TimeGAN en PyTorch
Reimplementación de TimeGAN ([Yoon et al., NIPS2019](https://papers.nips.cc/paper/8789-time-series-generative-adversarial-networks)) en PyTorch, desarrollada por 
[d9n13lt4n](https://github.com/d9n13lt4n/timegan-pytorch), en base al código original de [jsyoon0823](https://github.com/jsyoon0823/TimeGAN).

## Requisitos de instalación
Python3.8 y entorno Linux con GPU.
```bash
cat requirements.txt | xargs -n 1 pip install --upgrade
```

### structura de directorios
```bash
data/                         # datasets y script de preprocesamiento
  ├ data_preprocessing.py     # funciones de preprocesamiento
  └ stock.csv                 # dataset de ejemplo: datos bursátiles
metrics/                      # métricas de evaluación
  ├ dataset.py                # dataset para predecir caracte'risticas y un paso en el futuro
  ├ general_rnn.py            # modelo para ajustar los datos en la evaluación de tSTR
  ├ metric_utils.py           # evaluación de tSTR
  └ visualization.py          # implementaicón de PCA y t-SNE para series temporales
models/                       # código del modelo
output/                       # salida del modelo
main.py                       # código para entrenamiento y evaluación de TSTR del modelo
requirements.txt              # requerimientos para la ejecución
run.sh                        # bash para ejecutar el modelo
visualization.ipynb           # jupyter notebook para la visualización de datos y métricas
```
