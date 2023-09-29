# g3Caso3
### Santiago Alvarez Torres - Ariadna Tejedor Perez

## Conclusión KNN

Tras la primera prueba del modelo con una precisión inicial del 42%, el análisis del gráfico F1-Score reveló que la configuración óptima es con K=3. Este hallazgo fue confirmado por las gráficas de Voronoi, consolidando la eficacia de esta selección.

El análisis de la matriz de confusión refleja un desempeño óptimo del algoritmo, evidenciado por la clasificación precisa de todas las instancias en la clase 3, resultando en un verdadero-positivo y ausencia de errores de clasificación entre las clases. Este nivel de precisión se refleja en un F1-score máximo de 1.00, que representa un escenario ideal alcanzado con 38 vecinos. 

La precisión como el recall también alcanzan su máxima expresión de 1.00, confirmando la calidad y confianza en la clasificación del modelo. Es notable destacar que el F1-score se mantiene excepcionalmente alto, no descendiendo por debajo de aproximadamente 0.94 en el eje y, lo que sugiere un rendimiento sobresaliente en un rango de 0 a 38 vecinos, lo cual respalda la robustez y eficacia del algoritmo en esta configuración.

## Conclusión R. Logistica multinomial 

Se evidencia un desempeño destacado en la matriz de confusión, en la métrica de 'verdadero positivo.' Esto sugiere que cuando el valor real es positivo (por ejemplo, una especie de flor específica), el modelo de clasificación acertó al predecir que también era positivo. En otras palabras, cuando el modelo identifica una especie de flor en el conjunto de datos como positiva, coincide de manera precisa con la especie real de la flor, lo que indica una alta capacidad del modelo para reconocer las especies de flores de forma correcta y confiable.

El modelo de clasificación ha obtenido una presición del 100% en todas las clases siendo: 0-Setosa,1-Versicolor,2-Virginica. lo que significa que no cometio errores al realizar la clasificación de las flores, lo cual podríamos suponer que el modelo es altamente confiable para hacer la clasificación de las especies en función de las caracteristicas como longitud, ancho de los sepalos y petalos. Esto podría ser util para la empresa comercializadora de flores ya que le garantiza al cliente que reciban las flores de la especie que han pedido.

## R. Logistica vs KNN

A través del algoritmo de clasificación KNN, se determinó que la configuración más efectiva es K=3, especialmente considerando la base de datos iris que inicialmente tiene 3 categorías distintas ("Setosa", "Versicolor" y "Virginica"). KNN resulta ser un método apropiado en este contexto, ya que utiliza el F1-Score y las gráficas de Voronoi para ofrecer una comprensión más completa de la clasificación.

No obstante, es importante señalar que el desafío principal de KNN se presenta cuando no se tienen conocimientos previos sobre las categorías. En nuestro caso, nos enfrentamos al primer modelo propuesto por el método KNN, donde la primera prueba mostró una precisión inicial del 42%. Aunque las gráficas de Voronoi pueden proporcionar un análisis gráfico a través del F1-Score y Voronoi, en algunos casos no es la opción más óptima depender exclusivamente de estas representaciones gráficas. Además, cabe mencionar que la implementación de este enfoque requirió 37 celdas de código.

En contraste, la regresión logística multinomial ofrece un enfoque menos gráfico pero más numérico al utilizar umbrales de probabilidad para el análisis. Este método proporciona información valiosa a través de una tabla que indica la probabilidad de que una flor pertenezca a un tipo específico. A diferencia del método de clasificación KNN, donde esta especificidad no se muestra de manera directa. Además, es notable que la implementación de la regresión logística multinomial requiere menos código, con tan solo 12 celdas en comparación con las 37 necesarias para KNN.

## Recomendaciones para empresa comercializadora Iris

Si la empresa comercializadora de flores desea presentar la clasificación de su mercancía ante la junta directiva, se sugiere utilizar el método KNN, ya que proporciona una representación más intuitiva y fácil de comprender. Por otro lado, para un enfoque centrado en análisis preciso y eficiencia, se recomienda emplear la regresión logística multinomial, ideal para el ámbito analítico y de eficiencia.

Le recomendamos a la empresa que use la regresión logistica multinomial de la siguiente manera, con los resultados de probabilidades de predicción que permiten tomar decisiones, se podría hacer uso de un umbral, por ejemplo si establecemos un umbral de 0.5 podríamos hacer una clasificaicónd e la siguiente manera:

Si la probabilidad de predicción para la clase "Setosa" es mayor o igual a 0.5, se debe considerar que la observación pertenece a la clase "Setosa"
Si la probabilidad de predicción para la clase "Versicolor" es mayor o igual a 0.5, se debe considerar que la observación pertenece a la clase "Versicolor"
Si la probabilidad de predicción para la clase "Virginica" es mayor o igual a 0.5, se debe considerar que la observación pertenece a la clase "Virginica"

Por ejemplo: 
Extraemos la primera observación
[3.98128027e-03, 8.22150003e-01, 1.73868716e-01],

Se cumple que la probabilidad de predicción para la clase Versicolor es mayor a 0.5 siendo 0.83 por lo tanto podemos considerar que esta observación pertenece a la clase "Versicolor"

## Referencias

Arce, J. I. B. (2023). La matriz de confusión y sus métricas. Juan Barrios. https://www.juanbarrios.com/la-matriz-de-confusion-y-sus-metricas/

Jesús. (2019). Más allá del accuracy: precision, recall y F1. DataSmarts Español. https://datasmarts.net/es/mas-alla-del-accuracy-precision-recall-y-f1/

Multinomial Logistic Regression - Michael Fuchs Python. (2019, 15 noviembre). https://michael-fuchs-python.netlify.app/2019/11/15/multinomial-logistic-regression/

"Regresión logística multinomial ", Apuntes de clase 7 de INDU5012,Departamento de ingeniería y ciencias exactas, Universidad Sergio Arboleda, Septiembre 2023.