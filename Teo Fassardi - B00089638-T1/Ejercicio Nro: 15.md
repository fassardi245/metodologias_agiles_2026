# Ejercicio Nro: 15
## Enunciado
Generar un plan de trabajo basado en SCRUM para resolver la siguiente tarea Objetivo: El objetivo de este ejercicio es que los alumnos universitarios practiquen la creación de historias de usuario para un sistema informático de presupuesto de construcción de galpones, utilizando la metodología ágil. Descripción del ejercicio:

Los alumnos deberán formar equipos de trabajo, de preferencia de 3 a 5 personas por equipo.
Cada equipo deberá seleccionar la temática de construcción de galpones para su sistema informático de presupuesto.
Los equipos deberán generar al menos tres historias de usuario para su sistema, basadas en la temática seleccionada. Cada historia de usuario debe incluir un título y una descripción que contenga los criterios de aceptación.
Las historias de usuario deben enfocarse en las funcionalidades y características clave del sistema informático, considerando aspectos como la creación de presupuestos detallados, seguimiento del presupuesto durante la construcción, inclusión de etapas, generación de informes, entre otros.
Los equipos deben asegurarse de que las historias de usuario sean claras, concisas y comprensibles, siguiendo las buenas prácticas de redacción de historias ágiles.
Al finalizar, cada equipo deberá presentar sus historias de usuario al resto de la clase, explicando el contexto de su sistema y los criterios de aceptación de cada historia.
Se fomenta el intercambio de ideas y la retroalimentación constructiva entre los equipos durante las presentaciones. Nota: Los equipos pueden utilizar ejemplos y situaciones hipotéticas para desarrollar las historias de usuario, considerando las necesidades y requisitos típicos de un sistema de presupuesto de construcción de galpones. Además, se recomienda utilizar herramientas como tarjetas o post-its para escribir y visualizar las historias de usuario durante el ejercicio.

## Resolución

Historias de usuario

1. Carga de datos del cliente: Como usuario del sistema, quiero cargar los datos del cliente para asociar cada presupuesto a una persona o empresa determinada. El sistema deberá permitir ingresar nombre, teléfono, correo electrónico y dirección de la obra. Como criterios de aceptación, el nombre del cliente deberá ser obligatorio, los datos deberán guardarse correctamente y el presupuesto deberá quedar vinculado al cliente cargado.

2. Ingreso de medidas del galpón: Como usuario del sistema, quiero ingresar las medidas del galpón para calcular la superficie total de la construcción. El sistema deberá permitir cargar largo, ancho y altura, y con esos datos calcular automáticamente la superficie aproximada. Como criterios de aceptación, los valores ingresados deberán ser numéricos, no podrán ser menores o iguales a cero y el cálculo deberá actualizarse correctamente.

3. Selección del tipo de estructura: Como usuario del sistema, quiero seleccionar el tipo de estructura del galpón para que el presupuesto se adapte al tipo de construcción elegido. El sistema deberá ofrecer opciones como estructura metálica liviana, estructura metálica reforzada o estructura mixta. Como criterios de aceptación, el usuario deberá poder elegir una opción, modificarla antes de finalizar y esa selección deberá influir en el cálculo del presupuesto.

4. Cálculo de materiales: Como usuario del sistema, quiero que el sistema calcule los materiales necesarios para conocer el costo estimado de la obra. El sistema deberá estimar materiales como chapas, perfiles, columnas, vigas, tornillos, aislantes y portones según las medidas cargadas. Como criterios de aceptación, deberá mostrar cantidad, precio unitario, subtotal de cada material y el total general de materiales.

5. Cálculo de mano de obra: Como usuario del sistema, quiero calcular el costo de mano de obra para incluirlo dentro del presupuesto final. El sistema deberá permitir ingresar o calcular el costo de mano de obra según la superficie del galpón y el tipo de estructura seleccionada. Como criterios de aceptación, el usuario deberá poder modificar el valor, el sistema deberá calcular el total y ese importe deberá sumarse al presupuesto final.

6. División del presupuesto por etapas: Como usuario del sistema, quiero dividir el presupuesto por etapas de construcción para organizar mejor los costos de la obra. El sistema deberá separar el presupuesto en etapas como movimiento de suelo, estructura, cerramientos, techo, instalaciones y terminaciones. Como criterios de aceptación, cada etapa deberá mostrar sus costos asociados, su subtotal y el sistema deberá sumar todas las etapas en el total final.

7. Generación del informe final: Como usuario del sistema, quiero generar un informe final del presupuesto para entregárselo al cliente de manera clara y ordenada. El sistema deberá mostrar los datos del cliente, las medidas del galpón, el tipo de estructura, los materiales, la mano de obra, las etapas de construcción y el costo total. Como criterios de aceptación, el usuario deberá poder revisar el presupuesto antes de confirmarlo y el sistema deberá permitir imprimirlo o descargarlo.
