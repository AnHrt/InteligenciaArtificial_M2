# Inteligencia Artificial - Módulo 2

Entrega del módulo de **Deep Learning** en la concentración de *Inteligencia Artificial avanzada para la ciencia de datos*
###### María de los Angeles Arista Huerta - A01369984

### Entrega M2 Portafolio Implementación: ***Implementación de un modelo de deep learning.***
---
Se implementa un modelo para realizar la predicción tres razas de perros, las categorias son: *Doberman, Cocker y Saint Bernand*

El dataset utilizado para el entrenamiento y validación del modelo se obtuvo de kaggle, en el siguiente link se puede consultar: (solo se desargaron las imagenes de las razas mencionadas arriba)
> https://www.kaggle.com/datasets/jessicali9530/stanford-dogs-dataset?datasetId=119698&sortBy=voteCount

El dataset para las pruebas del modelo se encuentra en el siguiente link a drive:
> https://drive.google.com/drive/folders/1BAFNUikXyD0ZbhXLAf6RD9yRufo3SpfQ?usp=share_link

El video demostrativo del modelo y predicciones lo puede observar en el siguiente link a drive:
> https://drive.google.com/drive/folders/1WTOTwga2eemRTh441VFij3WRAACjlOxv?usp=share_link
---
La notebook ***A01369984_DP_M1.ipynb*** contiene el primer modelo empleado de una red convolusional.

La notebook ***A01369984_DP_M2.ipynb*** contiene el modelo empleado de transfer learning (VGG16).

La notebook ***A01369984_M2_Pred.ipynb*** contiene el codigo con las predicciones realizadas.

---
### Modelos empleados
> Primer modelo
 * train acc: *0.34* 
 * val acc:   *0.36*
 * test acc:  *0.27*
> Modelo intermedio con vgg16
 * train acc: *0.74* 
 * val acc:   *0.63*
 * test acc:  *0.5*
> Modelo final vgg16
 * train acc: *0.80* 
 * val acc:   *0.87*
 * test acc:  *0.97*

En el modelo intermedio se implemento transfer learning de vgg16.

Se agregaron modificaciones en las imagenes al ser generadas:
							* horizontal_flip = True,
							* rotation_range = 45,
							* shear_range = 0.2,
							* zoom_range = 0.2

Se agregó una capa de *GlobalAveragePooling2D*

En el modelo final de vgg16 se agrego un dropout(0.5) y se modifico la capa Dense(256,activation='relu') a Dense(128,activation='relu')
