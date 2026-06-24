# Ejercicio Nro: 15

## Enunciado
Generar un plan de trabajo basado en SCRUM para resolver la siguiente tarea:

**Objetivo:** El objetivo de este ejercicio es que los alumnos universitarios practiquen la creación de historias de usuario para un sistema informático de presupuesto de construcción de galpones, utilizando la metodología ágil.

**Descripción del ejercicio:**
1. Los alumnos deberán formar equipos de trabajo, de preferencia de 3 a 5 personas por equipo.
2. Cada equipo deberá seleccionar la temática de construcción de galpones para su sistema informático de presupuesto.
3. Los equipos deberán generar al menos tres historias de usuario para su sistema, basadas en la temática seleccionada. Cada historia de usuario debe incluir un título y una descripción que contenga los criterios de aceptación.
4. Las historias de usuario deben enfocarse en las funcionalidades y características clave del sistema informático, considerando aspectos como la creación de presupuestos detallados, seguimiento del presupuesto durante la construcción, inclusión de etapas, generación de informes, entre otros.
5. Los equipos deben asegurarse de que las historias de usuario sean claras, concisas y comprensibles, siguiendo las buenas prácticas de redacción de historias ágiles.
6. Al finalizar, cada equipo deberá presentar sus historias de usuario al resto de la clase, explicando el contexto de su sistema y los criterios de aceptación de cada historia.
7. Se fomenta el intercambio de ideas y la retroalimentación constructiva entre los equipos durante las presentaciones.

*Nota: Los equipos pueden utilizar ejemplos y situaciones hipotéticas para desarrollar las historias de usuario, considerando las necesidades y requisitos típicos de un sistema de presupuesto de construcción de galpones. Además, se recomienda utilizar herramientas como tarjetas o post-its para escribir y visualizar las historias de usuario durante el ejercicio.*

---

## Resolución

### Parte 1: Plan de Trabajo basado en SCRUM (Adaptación Académica)

Para abordar la actividad de manera ágil en un bloque de clase, el equipo de 5 personas se organizará simulando un **Sprint único de corta duración**, distribuyendo roles y ceremonias de la siguiente manera:

#### 1. Roles de Scrum
* **Product Owner / Scrum Master (Compartido/Rotativo):** Un integrante moderará el debate para asegurar que se cumplan las prioridades del presupuesto de galpones y se respeten los tiempos del bloque.
* **Development Team (Equipo de Desarrollo):** El resto de los integrantes participará activamente en la lluvia de ideas, redacción de criterios de aceptación y preparación del soporte visual (tarjetas/post-its).

#### 2. Eventos del Sprint (Distribución del tiempo)
* **Sprint Planning (5 minutos):** Definición del alcance. Selección de los módulos clave del sistema de galpones que se van a transformar en historias (datos, medidas, cálculo de costos, etapas, informes).
* **Sprint Execution / Desarrollo del Backlog (15 minutos):** Redacción colaborativa de las historias de usuario utilizando tarjetas físicas o digitales. Aplicación de las plantillas ágiles y definición de los Criterios de Aceptación (DoD - *Definition of Done*).
* **Sprint Review & Retrospective (10 minutos):** Simulación interna de la presentación grupal, revisión final de que ninguna historia quede ambigua y feedback rápido antes de exponer frente al profesor.

---

### Parte 2: Product Backlog (Historias de Usuario)

A continuación, se presentan las historias de usuario detalladas que componen el alcance del sistema informático de presupuestos:

#### 1. Carga de datos del cliente
* **Descripción:** Como usuario del sistema, quiero cargar los datos del cliente para asociar cada presupuesto a una persona o empresa determinada. El sistema deberá permitir ingresar nombre, teléfono, correo electrónico y dirección de la obra.
* **Criterios de Aceptación:**
  * El nombre del cliente deberá ser un campo obligatorio.
  * Los datos deberán guardarse correctamente en el estado del presupuesto.
  * El presupuesto generado deberá quedar vinculado unívocamente al cliente cargado.

#### 2. Ingreso de medidas del galpón
* **Descripción:** Como usuario del sistema, quiero ingresar las medidas del galpón para calcular la superficie total de la construcción. El sistema deberá permitir cargar largo, ancho y altura, y con esos datos calcular automáticamente la superficie aproximada.
* **Criterios de Aceptación:**
  * Los valores ingresados deberán ser estrictamente numéricos.
  * No se permitirán valores menores o iguales a cero.
  * El cálculo de la superficie debe actualizarse automáticamente en pantalla al modificar las medidas.

#### 3. Selección del tipo de estructura
* **Descripción:** Como usuario del sistema, quiero seleccionar el tipo de estructura del galpón para que el presupuesto se adapte al tipo de construcción elegido. El sistema deberá ofrecer opciones como estructura metálica liviana, estructura metálica reforzada o estructura mixta.
* **Criterios de Aceptación:**
  * El usuario deberá poder elegir una única opción mediante un selector claro.
  * Se debe permitir modificar la selección antes de finalizar el presupuesto.
  * La opción elegida debe alterar directamente los coeficientes de cálculo del costo final.

#### 4. Cálculo de materiales
* **Descripción:** Como usuario del sistema, quiero que el sistema calcule los materiales necesarios para conocer el costo estimado de la obra. El sistema deberá estimar materiales como chapas, perfiles, columnas, vigas, tornillos, aislantes y portones según las medidas cargadas.
* **Criterios de Aceptación:**
  * Debe desglosar dinámicamente la cantidad, precio unitario y subtotal de cada material.
  * Debe computar y mostrar un total general exclusivo para la sección de materiales.

#### 5. Cálculo de mano de obra
* **Descripción:** Como usuario del sistema, quiero calcular el costo de mano de obra para incluirlo dentro del presupuesto final. El sistema deberá permitir ingresar o calcular el costo de mano de obra según la superficie del galpón y el tipo de estructura seleccionada.
* **Criterios de Aceptación:**
  * El usuario debe tener la opción de sobrescribir o modificar manualmente el valor sugerido de mano de obra.
  * El sistema deberá calcular el total de este concepto y sumarlo de forma transparente al importe neto general.

#### 6. División del presupuesto por etapas
* **Descripción:** Como usuario del sistema, quiero dividir el presupuesto por etapas de construcción para organizar mejor los costos de la obra. El sistema deberá separar el presupuesto en etapas como movimiento de suelo, estructura, cerramientos, techo, instalaciones y terminaciones.
* **Criterios de Aceptación:**
  * Cada etapa constructiva deberá reflejar sus propios costos asociados y subtotal visible.
  * La sumatoria matemática de todas las etapas debe coincidir exactamente con el valor del total final expuesto al cliente.

#### 7. Generación del informe final
* **Descripción:** Como usuario del sistema, quiero generar un informe final del presupuesto para entregárselo al cliente de manera clara y ordenada. El sistema deberá mostrar los datos del cliente, las medidas del galpón, el tipo de estructura, los materiales, la mano de obra, las etapas de construcción y el costo total.
* **Criterios de Aceptación:**
  * El usuario deberá contar con una pantalla de vista previa para revisar la información antes de confirmarla.
  * El sistema debe habilitar una acción directa para exportar el informe (imprimirlo o descargarlo en formato PDF).
