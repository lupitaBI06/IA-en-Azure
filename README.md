# Inteligencia Artificial en Azure

La Inteligencia Artificial (IA) es la rama de la informática que adapta y mejora su capacidad de toma de decisiones a lo largo del tiempo en función de sus éxitos y errores. El objetivo de la IA es crear un sistema de software que pueda adaptarse o aprender algo por sí mismo sin estar programando explícitamente para hacerlo.

Existen dos enfoques para la IA:

- **Aprendizaje profundo**: Se modela en la red neuronal de la mente humana, lo que le permite descubrir, aprender y crecer a través de la experiencia.

- **Aprendizaje automático**: Usa los datos existentes para entrenar un modelo, probarlo y aplicaro a nuevos datos para pronosticar comportamientos, resultados y tendencias futuros.

En Azure se tienen tres principales servicios:

- ### Azure Machine Learning (ML)

![Logo Azure Machine Learning](Imagenes\AMLlogo.png)

Es una plataforma que se usa para realziar predicciones o clasificaciones. Se puede implementar y usar modelos de ML en tiempo real a través de API web. Con ML se pueden realizar:

- **Obtener los datos**
 - Tratar los datos que faltan o incorrectos.
 - Separar los datos en entrernamiento y prueba.
 - Enviar datos al proceso de entrenamiento.
- **Entrenar y evaluar modelos**
- **Crear canalizaciones que definen dónde y cuándo ejecutar los experimentos**
- **Implementar el algoritmo con una API en un punto de conexión**

Se recomienda seleccionar el servicio Azure ML cuando se requiere tener un control completo sobre el diseño y el entrenamiento con propios datos.

**Ejemplo de uso de Azure ML**

- Desde [ml.azure.com](ml.azure.com) crear un nuevo recurso.
![Crear ML automatizaod](Imagenes\creaciondelMLAutomatizado.PNG)
- Crear instancia de proceso (Máquina Virtual). 
![Crear instancia](Imagenes\crearinstancia.PNG)
 - En la creación la región se encuentra bloqueada por que en ML las máquinas virtuales deben estar en la misma región. 
 - Se puede elegir entre CPU y GPU, utilizar GPU cuando se necesite mas procesamiento.
- Ya que se tiene creada la máquina virtual se cargan los datos en la sección datos, le damos en crear desde archivos web. En este caso se utilizó una base de datos de un excel al que se puede acceder mediante el siguiente link [https://aka.ms/bike-rentals](https://aka.ms/bike-rentals).
![seleccionar datos](Imagenes\databasedatosbasicos.PNG)
![settings de datos](Imagenes\settingspreview.PNG)

- crado el conjunto de datos creamos un ML Automatizado que se encuentra en el panel izquierdo.
![crear ML automatizado](Imagenes\MLautimatizado.PNG)
 - En datos seleccionamos el dataset creado de las bicis.
 - Creamos un clúster de proceso desde la pestaña procesos (Máquina virtual que sirve para crear Machine Learning).
  ![Crear cluster de proceso](Imagenes\clusterprocesocrear.PNG)
  ![Configuracion avanzada de cluster de proceso](Imagenes\advancesettingscluster.PNG)
 - En Azure ML se crean experimentos, que son intentos de modelos, en los que se pueden hacer varios experimentos para ver cuál da menjor resultado y de ahí crear el modelo. La columna destino es mi columna de etiquetas. Se selecciona el clúster de proceso creado anteriormente y se da en siguiente.

 El siguiente paso es seleccionar la tarea y configuración en donde vamos a determianr su se va a clasificar, predecir, hacer procesamiento de lenguaje natural etc. En este caso estamos haciendo una predicción.

 El último paso es seleccionar si se tiene un set de datos para prueba, o si se quiere dividir el data set en entrenamiento y prueba y se da en crear.

![configuracion ML automatizado](Imagenes\validacionytest.PNG)

- Finalmente se muestra el recurso creado ejecutandose.

![Creacion finalizada](Imagenes\creaciondelMLAutomatizado.PNG)
 
- Para ver los resultados damos clic en experimento

