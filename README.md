# Arboles de decision

Análisis de clasificación mediante Árboles de decisión que permita desarrollar un modelo predictivo para averiguar qué medicamento podría ser apropiado para un futuro paciente

Comenzamos cargando la base de datos a utilizar para conocer el mejor medicamento a utilizar segun los parametros de un paciente
<br>![image](https://github.com/user-attachments/assets/811663e5-c204-4c16-9b6d-f39461f201d9)

Separamos los parámetros de entrenamiento de los resultados que necesitamos determinar y los codificamos a valores que podamos procesar con mayor facilidad
<br>![image](https://github.com/user-attachments/assets/d269a53c-187e-4d82-ac49-370cc1da04c6)

Convirtiendo todo a datos numéricos
<br>![image](https://github.com/user-attachments/assets/1af72ef0-a15a-49e7-ba4b-30b29727641d) ![image](https://github.com/user-attachments/assets/e4aadffa-37f3-4a68-989d-3b9378f30c4f)

Realizamos la asignación de grupos de prueba y entrenamiento para poder procesar los datos con el modelo deseado
<br>![image](https://github.com/user-attachments/assets/66c45d13-0c80-4289-a772-d7dc62653be2)

***Criterio Gini***

Utilizamos primero el criterio Gini obteniendo los siguientes resultados
<br>![image](https://github.com/user-attachments/assets/7e23aacc-7a84-4825-b249-54fb0a43ca80) ![image](https://github.com/user-attachments/assets/54ee759b-af58-4909-8159-7db71a0ceb6c)

Al utilizar una base de entrenamiento de .2, el criterio Gini y sin definir una máxima profundidad, obtenemos resultados 100% certeros, lo que puede indicar que el modelo está haciendo overfitting que en este caso puede resultar en la memorización de la información en lugar de generalizar patrones.
Después de ajustar los parámetros a una base de entrenamiento de .3, criterio Gini y definir una máxima profundidad de 5 obtenemos una pequeña variación en los datos lo que nos indica que puede estar funcionando mejor pero aún se necesita mejorar el uso del modelo.

<br>![image](https://github.com/user-attachments/assets/c6b90d91-8e07-4228-a5af-1d29ba189f13)
<br>![image](https://github.com/user-attachments/assets/6004ac34-63dc-4436-8017-9f4658665088)

Con el modelo Gini, un máximo de profundidad de 3 resulta muy poco para poder llegar a una conclusión, pero solo necesita 4 para generar el resultado, el árbol comienza evaluando primero si el valor de Na a K es menor o igual a 14.839, si resulta falso determina que el medicamento Y es el más adecuado, si es verdad procede a evaluar la presión sanguínea midiendo si es menor o igual a 0.5, si resulta verdad, el modelo determina que el medicamento A es el apropiado si la edad es menor o igual a 53, si no, determina el medicamento B.
Si en el paso anterior la presión sanguínea es mayor a 0.5, vuelve a evaluar si es menor o igual a 1.5, si resulta falso determina que el medicamento X es el adecuado, si no determina si el colesterol es mayor a 0.5 el medicamento X sigue siendo el adecuado, si no, el medicamento C es el adecuado.

***Criterio Entropia***

Probamos ahora con el criterio Entropy
<br>![image](https://github.com/user-attachments/assets/02fd73cb-6d5e-49a2-bbee-817bdc3c2736)

Obtenemos la siguiente información
<br>![image](https://github.com/user-attachments/assets/ce407db8-f2d1-40c7-a64f-786369adddd1)

Al utilizar el clasificador Entropy obtenemos diferentes valores para los clasificadores pero el mismo resultado en cuanto a las predicciones y la misma matriz de confusión, por lo que mi conclusion seria que podemos utilizar cualquiera de los dos resultados generados pero para mejorar la predicción necesitamos conseguir más información o probar con un modelo diferente.
<br>![image](https://github.com/user-attachments/assets/ee4b059f-5a57-4417-8c53-1bf493d8d8be)

El árbol de decisión generado con el criterio entropy da los mismos resultados con el valor del criterio siendo la única diferencia en este caso.

<br>![image](https://github.com/user-attachments/assets/28f4f335-90aa-45ed-af4e-bbfa82ab895d)
