# TP3 Redes CNN-Cifar-100
## Alumna
Anna Candela Gioia Perez





Se implementó una red nueronal convolucional con distintos métodos de regularización y de preoprocesamiento para el dataset de cifar100. En este caso se logró un score de 64% aproximadamente. 

## Librerías utilizadas
Los recursos utilizados fueron:
* Matplolib
* PyTorch
* Keras
* Numpy


## Proceso 
Se intentaron un montón, unas de las cosas que mejroaron es aplciar el batchnormalization en las convolucionales y el DropOut en las densas. También, se intentaron varios métodos de DataAugmentation, pero sólo mejoró con RandomCutout (igual se dejó en código los usados). 
También se intentaron usar varios elementos como DropBlock, pero no mejoraron. 
### CNN_Cifar_100_58: 
* ImageGenerator
* Convolucionales con batchnormalization y activación relu
* Capas densas con dropout y batchnormalization y activación relu
### CNN_Cifar_100_62: 
* ImageGenerator
* Convolucionales con batchnormalization y activación swish
* Capas densas con dropout y batchnormalization y activación swish

### CNN_Cifar_100_63:
* ImageGenerator
* Convolucionales con batchnormalization y activación swish
* Capas densas con dropout (con MaxNorm(4)) y batchnormalization y activación swish

### CNN_Cifar_100_64:
* ImageGenerator + DataAgumentatio con RandomCutout
* Convolucionales con batchnormalization y activación swish
* Capas densas con dropout (con MaxNorm(4)) y batchnormalization y activación swish

### CNN_Cifar_100_64_GaussianNoise:
* ImageGenerator + DataAgumentatio con RandomCutout
* Convolucionales con batchnormalization y activación swish + GaussianNoise
* Capas densas con dropout (con MaxNorm(4)) y batchnormalization y activación swish

## Cifar_100_CNN_
* ImageGenerator + DataAgumentatio con RandomCutout 
* Convolucionales con batchnormalization y activación swish
* Capas densas con dropout (con MaxNorm(4)) y batchnormalization y activación swish
