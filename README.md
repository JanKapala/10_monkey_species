Dataset: monkeys - 10 classes. Continous augmentation has been applied. There ar batches of size 64.

Three models has been trained. First of them achived near 75& accuraccy after ~1000 epoches (not visible in output cell because of multiple rerun). It uses dropout, batch normalization and regularization L2. Second model uses no dropout at all and much less L2 regularization (0.001 vs 0.03). It also uses adam optimizer instead of SGD with momentum. It learns faster but it also overfit faster, so there were no difference from efficiency point of view.

Last, third, model has fine tuned hyperparameters: no regularization L2, dropout=0.25, no batch normalization. I has very quickly (~20 epochs) achieved 75% accuraccy and then it starts oscillate near it. Finally it achieves 83%. Maybe longer training could improve accuraccy to 85-90%.

Monkeys dataset has 10 classes so it is much harder than binary classification so this performance is quite good.

Feature maps analysis of all 3 models shows that a lot of kernels seems to do nothing (some of the feature maps are totally white or black)
