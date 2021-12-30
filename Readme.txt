		Framework en data science
_____________________________________________________
La terminologia en Data science es:

Datos: unidades de información o realizacion de la observacion

Feature : Tipo de información de acuerdo a sus caracteristicas

Filas : observaciones  individuales o muestras

Columnas : caracteristicas que describen las observaciones

Outlier : Son datos atipicos de la muestras

Pre-processing : La preparacion de los datos para aplicar un modelo de ML

_____________________________________________________


Hot encoder es usado para convertir de un conjunto de etiquetas
categiricas convertirlas en un vector.

creando un vector x=(x1,x2,...,xn) tal que cada xi es 0 o 1 es el estado en que se 
encuentra 

------------------------------------------------------------------------------------
Procesamiento de datos

. dropna() removerá la fila si una sola columna individual tiene un feature faltante. 
De forma alternativa puedes especificar si este es el acercamiento indicado, o si quieres
eliminar solo filas donde falte toda la información de la columna.


_____________________________________________________
 Representando patrones en tus datos

Dado nuestro dataset queremos ser capaces de decir si alguien tiene o no diabetes, 
indicado por la columna outcome.

Un 1 indica que el paciente tiene diabetes, donde 0 sugiere que no la tiene.
Queremos aprender si las condiciones pre-existentes (age, blood-pressure, insulin, BMI)
pueden contribuir a la diabetes.

Usaremos histogramas y gráficas de dispersión para ver cómo se comportan los grupos/población
 de nuestros datos. Es bueno hacer esto antes de construir un modelo.
_____________________________________________________
Representando patrones en tus datos - histogramas


Primero revisa las distribuciones de frecuencia. Para esto utilizarás un histograma.

Un histograma usa bins o límites de un valor numérico.
Contamos cuántas filas caen dentro de los límites superior e inferios de cada bin y esto crea 
la distribución.

Pandas puede automatizar la creación de histogramas para no contar desde cero.
Puedes darle el número de bins o esquinas de los bins (el criterio para límites inferior y superior).
Para nuestro caso utiliza el predeterminado (que generalmente es 10 bins).
Dado que queremos aprender el estado de si la persona tiene o no diabetes, 
podemos preguntar si nuestros datos están bien distribuidos en valores de 1 o 0 para el outcome.
Necesitamos clases igualmente balanceadas para hacer predicciones decentes.


_____________________________________________________

Receta de algoritmos de ML

	-1 Proceso de decision: Como los modelos hacen una prediccion usando los parametros

	-2 Funcion de error/coste : Como evaluar si 	los parametros en el modelo son buenos

	-3 Reglas de actualización : Como mejorar los parámetros para hacer mejores predicciones

_____________________________________________________

		Normalizacion de datos
_____________________________________________________

Dado el conjunto de datos \{x1,x2,...,xn\} se generan los datos normalizados
\{z1,z2,...,zn\} donde zi=(xi-\mu)/\sigma

