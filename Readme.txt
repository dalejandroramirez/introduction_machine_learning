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
_____________________________________________________

				Matriz de confusion
_____________________________________________________
Esta matriz sirve para estimar el error que existe
en los modelos logisticos donde

________________________________________________
|		     |  Actually		| Actually		|
|			 |  Positive(1)		| Negative(0)	|
|____________|__________________|_______________|
|Predicted   |	True Positive	| 	False		|
|positive(1) |		(TP)		|	Positive	|
|____________|__________________|_____(FP)______|
|Predicted   |	False Negative	| 	True		|
|Negative(0) |		(FN)		|	Negative	|
|____________|__________________|____(TN)_______|


ACCURACY=(TP+FN)/(TP+FN+FP+TN)
_________________________________________________________________

¿Como etiquetar una nueva columna?
__________________________________________________________________
datos: solo los atributos de los objetos

data.nombre: es un array con los nombres de las columnas

# Creamos el DataFrame con los feature names.
data = pd.DataFrame(data=datos, columns=data.nombres)

# Creamos el DataFrame con los targets (las especies de la flor).
target = pd.DataFrame(data=datosnuevos, columns=['nombre_dato_new'])

# Unimos ambos DF con concat; agregamos una nueva columna.
data = pd.concat([data, target], axis=1)
____________________________________________________________________

				Redes neuronales
____________________________________________________________________
- Deep Feed-forward (DNNs)
	.Estas  usan funciones de activacion que son perfectas para solucionar
	problemas no lineales

	. evaluar las funciones en cada nodo



- Comvolutional (CNNs)
	.operador comvolucional pool o kernel
	. Usado en imagenes y genómicos
	
- Recurrente (RNNs)
	.Neuronas que tienen larga memoria, por ejemplo informacion de lenguaje

_________________________________________________________________

Deed feed-forward

va calculando una por una las funciones de los nodos  
para posteriormente pensar en la funcion de perdida
que si es regresion es con media cuadratica
y si es clsificacion con el clossentropy

_________________________________________________________________

Backpropagation
_________________________________________________________________
Una vez que se haya escogido la 
Esta es la regla de actualizacion usado para ajustar los pesos en las Redes

Este inicia desde la salida hasta los datos de entrada

actualizadno los datos tomando la derivada parcial de ellos con respecto a cada nodo.

empezando desde la salida hacia atras hasta la entrada


