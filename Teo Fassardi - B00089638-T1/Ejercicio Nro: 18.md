# Ejercicio Nro. 18 - Scrum con IA
## Consigna

Crear una serie de cinco prompts que simulen las principales etapas y actividades de Scrum aplicadas al desarrollo de una aplicación web para una empresa de logística.

Cada prompt debe utilizar como entrada el resultado obtenido en el prompt anterior, formando una secuencia lógica:

Definición del Product Backlog.
Planificación del Sprint.
Ejecución del Sprint.
Revisión del Sprint.
Retrospectiva del Sprint.

Cada prompt debe incluir:

La descripción de la actividad Scrum.
El contexto.
Las instrucciones.
Los datos de entrada.
El resultado esperado.
El resultado obtenido al aplicar el prompt.
Las técnicas de prompting utilizadas.
## Resolución

## Prompt 1: Definición del Product Backlog

### Actividad Scrum a simular

En esta etapa se simula la definición inicial del Product Backlog para una aplicación web de gestión logística. El objetivo es transformar los requerimientos del cliente en historias de usuario claras, ordenadas por prioridad.

### Prompt desarrollado

Actúa como Product Owner de un proyecto Scrum para una empresa de logística.

Contexto:
La empresa necesita una aplicación web para gestionar envíos, clientes, transportistas y seguimiento de paquetes. El sistema debe permitir registrar usuarios, cargar nuevos envíos, consultar el estado de cada envío, generar reportes y notificar cambios importantes a los clientes.

Instrucción:
A partir de estos requerimientos iniciales, crea un Product Backlog inicial con historias de usuario prioritarias.

Input:
- Registro e inicio de sesión de usuarios.
- Carga de nuevos envíos.
- Seguimiento del estado de los envíos.
- Gestión de clientes.
- Gestión de transportistas.
- Reportes de envíos.
- Notificaciones al cliente cuando cambia el estado del envío.

Output esperado:
Genera una tabla con las columnas: ID, historia de usuario, prioridad, criterio de aceptación y observaciones.

### Resultado de aplicar el prompt

| ID | Historia de usuario | Prioridad | Criterio de aceptación | Observaciones |
|---|---|---|---|---|
| HU01 | Como usuario, quiero registrarme e iniciar sesión para acceder al sistema de forma segura. | Alta | El usuario puede crear una cuenta, iniciar sesión y cerrar sesión correctamente. | Necesario para controlar el acceso. |
| HU02 | Como operador logístico, quiero cargar nuevos envíos para registrar paquetes dentro del sistema. | Alta | El sistema permite ingresar datos del remitente, destinatario, dirección y tipo de envío. | Es una función central del sistema. |
| HU03 | Como cliente, quiero consultar el estado de mi envío para saber dónde se encuentra mi paquete. | Alta | El cliente puede buscar un envío mediante un código de seguimiento. | Mejora la experiencia del cliente. |
| HU04 | Como administrador, quiero gestionar clientes y transportistas para mantener actualizada la información operativa. | Media | El sistema permite crear, editar y eliminar clientes y transportistas. | Puede realizarse luego de las funciones principales. |
| HU05 | Como administrador, quiero generar reportes de envíos para analizar el rendimiento del servicio. | Media | El sistema genera reportes por fecha, estado y transportista. | Aporta información para la toma de decisiones. |
| HU06 | Como cliente, quiero recibir notificaciones cuando cambie el estado de mi envío para estar informado sin ingresar al sistema. | Baja | El sistema envía una notificación cuando el envío cambia de estado. | Puede incorporarse en un sprint posterior. |

### Técnicas utilizadas
- Contextualización del rol: se le indica a la IA que actúe como Product Owner.
- Definición de contexto: se explica el tipo de empresa y el objetivo del sistema.
- Clasificación de requerimientos: se transforman necesidades generales en historias de usuario.
- Priorización: se ordenan las historias según su importancia.
- Formato de salida: se solicita una tabla para que el resultado sea claro y fácil de usar.

## Prompt 2: Planificación del Sprint

### Actividad Scrum

En la planificación del Sprint, el equipo selecciona las historias de usuario prioritarias del Product Backlog y las divide en tareas. También establece responsables, estimaciones y un objetivo para el Sprint.

### Prompt

**Contexto:**  
Eres el Scrum Master de un equipo que desarrolla una aplicación web para una empresa de logística. Debes organizar un Sprint de dos semanas tomando como entrada el Product Backlog generado anteriormente.

**Instrucción:**  
Analiza las historias de usuario del Product Backlog. Selecciona las que tengan mayor prioridad y puedan desarrollarse durante el Sprint. Crea un plan que incluya el objetivo del Sprint, las tareas necesarias, sus responsables y una estimación en puntos de historia.

**Entrada:**

| ID | Historia de usuario | Prioridad |
|---|---|---|
| HU01 | Como usuario, quiero registrarme e iniciar sesión para acceder al sistema. | Alta |
| HU02 | Como operador, quiero crear un envío para gestionar su entrega. | Alta |
| HU03 | Como cliente, quiero consultar el estado de mi envío para conocer su situación. | Alta |
| HU04 | Como administrador, quiero gestionar clientes y transportistas. | Media |
| HU05 | Como usuario, quiero generar reportes sobre los envíos. | Media |
| HU06 | Como cliente, quiero recibir notificaciones sobre cambios en mi envío. | Baja |

**Salida esperada:**

Un plan para un Sprint de dos semanas que contenga:

- Objetivo del Sprint.
- Historias de usuario seleccionadas.
- Tareas necesarias.
- Responsables.
- Estimación en puntos de historia.

### Resultado obtenido

**Objetivo del Sprint:**  
Desarrollar las funciones principales que permitan a los usuarios acceder al sistema, registrar envíos y consultar su estado.

| Tarea | Historia | Descripción | Responsable | Puntos |
|---|---|---|---|---:|
| T01 | HU01 | Diseñar las pantallas de registro e inicio de sesión. | Diseñador UX/UI | 2 |
| T02 | HU01 | Implementar el registro y la autenticación de usuarios. | Desarrollador A | 5 |
| T03 | HU02 | Diseñar el formulario para crear envíos. | Diseñador UX/UI | 2 |
| T04 | HU02 | Implementar el registro de nuevos envíos. | Desarrollador B | 5 |
| T05 | HU03 | Crear la consulta mediante código de seguimiento. | Desarrollador C | 5 |
| T06 | HU01, HU02 y HU03 | Realizar pruebas funcionales y corregir errores. | Tester QA | 3 |

**Total estimado:** 22 puntos de historia.

Las historias HU04, HU05 y HU06 permanecen en el Product Backlog para futuros Sprints.

### Técnicas utilizadas

- Asignación de rol mediante la figura del Scrum Master.
- Encadenamiento de prompts mediante el Product Backlog anterior.
- Priorización de historias de usuario.
- Descomposición de historias en tareas.
- Estimación con puntos de historia.
- Definición estructurada del formato de salida.

## Prompt 3: Ejecución del Sprint

### Actividad Scrum

Durante la ejecución del Sprint, el equipo desarrolla las tareas seleccionadas en la planificación. También realiza pruebas y registra el estado de cada tarea para obtener un incremento funcional del producto.

### Prompt

**Contexto:**  
Eres el líder técnico de un equipo Scrum que desarrolla una aplicación web para una empresa de logística. El equipo debe ejecutar el plan definido para un Sprint de dos semanas.

**Instrucción:**  
Analiza el siguiente plan del Sprint y simula su ejecución. Indica el estado final de cada tarea, las funcionalidades implementadas, las pruebas realizadas y los posibles errores encontrados. Finalmente, describe el incremento de software funcional obtenido.

**Entrada:**

**Objetivo del Sprint:**  
Desarrollar las funciones principales que permitan a los usuarios acceder al sistema, registrar envíos y consultar su estado.

| Tarea | Historia | Descripción | Responsable | Puntos |
|---|---|---|---|---:|
| T01 | HU01 | Diseñar las pantallas de registro e inicio de sesión. | Diseñador UX/UI | 2 |
| T02 | HU01 | Implementar el registro y la autenticación de usuarios. | Desarrollador A | 5 |
| T03 | HU02 | Diseñar el formulario para crear envíos. | Diseñador UX/UI | 2 |
| T04 | HU02 | Implementar el registro de nuevos envíos. | Desarrollador B | 5 |
| T05 | HU03 | Crear la consulta mediante código de seguimiento. | Desarrollador C | 5 |
| T06 | HU01, HU02 y HU03 | Realizar pruebas funcionales y corregir errores. | Tester QA | 3 |

**Total estimado:** 22 puntos de historia.

**Salida esperada:**

- Estado final de cada tarea.
- Funcionalidades implementadas.
- Pruebas realizadas.
- Errores o dificultades encontradas.
- Descripción del incremento funcional obtenido.

### Resultado obtenido

#### Estado de las tareas

| Tarea | Resultado | Estado |
|---|---|---|
| T01 | Se diseñaron las pantallas de registro e inicio de sesión. | Completada |
| T02 | Se implementó el registro, inicio y cierre de sesión. | Completada |
| T03 | Se diseñó el formulario para registrar nuevos envíos. | Completada |
| T04 | Se implementó la creación de envíos con un código de seguimiento único. | Completada |
| T05 | Se desarrolló la consulta del estado de un envío mediante su código. | Completada |
| T06 | Se realizaron pruebas funcionales y se corrigieron los errores detectados. | Completada |

#### Funcionalidades implementadas

- Registro de nuevos usuarios.
- Inicio y cierre de sesión.
- Creación de envíos.
- Generación de un código único de seguimiento.
- Consulta del estado de un envío.
- Validación de los datos ingresados en los formularios.

#### Pruebas realizadas

| Prueba | Resultado |
|---|---|
| Registro con datos válidos | Exitoso |
| Registro con un correo ya utilizado | El sistema muestra un mensaje de error |
| Inicio de sesión con datos correctos | Exitoso |
| Inicio de sesión con contraseña incorrecta | El acceso es rechazado |
| Creación de un envío con datos completos | Exitoso |
| Consulta con un código válido | Se muestra el estado del envío |
| Consulta con un código inexistente | El sistema informa que el envío no existe |

#### Errores encontrados y corregidos

- Se corrigió la validación de correos electrónicos duplicados.
- Se solucionó un error que permitía crear envíos con campos vacíos.
- Se mejoró el mensaje mostrado al ingresar un código de seguimiento inexistente.

#### Incremento funcional obtenido

Al finalizar el Sprint, se obtuvo una primera versión funcional de la aplicación. Los usuarios pueden registrarse, iniciar sesión, crear un nuevo envío y consultar su estado mediante un código de seguimiento.

Este incremento cumple con las historias de usuario HU01, HU02 y HU03 seleccionadas durante la planificación del Sprint.

### Técnicas utilizadas

- Asignación del rol de líder técnico.
- Encadenamiento mediante el plan generado en el Prompt 2.
- Simulación de la ejecución del Sprint.
- Seguimiento del estado de las tareas.
- Validación mediante casos de prueba.
- Descripción estructurada del incremento funcional.

## Prompt 4: Revisión del Sprint

### Actividad Scrum

Durante la revisión del Sprint, el equipo presenta el incremento funcional al cliente. El objetivo es comprobar si las funcionalidades desarrolladas cumplen con sus necesidades, recibir retroalimentación y registrar posibles mejoras para los próximos Sprints.

### Prompt

**Contexto:**  
Eres el Product Owner de un equipo Scrum que desarrolla una aplicación web para una empresa de logística. El equipo ha finalizado el Sprint y debe presentar al cliente el incremento funcional obtenido.

**Instrucción:**  
Analiza el incremento funcional desarrollado. Simula una reunión de revisión del Sprint con el cliente e indica las funcionalidades aceptadas, las observaciones realizadas, las nuevas solicitudes y las lecciones aprendidas por el equipo.

**Entrada:**

Al finalizar el Sprint, se obtuvo una primera versión funcional de la aplicación con las siguientes características:

- Registro de nuevos usuarios.
- Inicio y cierre de sesión.
- Creación de envíos.
- Generación de un código único de seguimiento.
- Consulta del estado de un envío.
- Validación de datos en los formularios.

También se realizaron pruebas funcionales y se corrigieron errores relacionados con correos duplicados, campos vacíos y códigos de seguimiento inexistentes.

**Salida esperada:**

- Funcionalidades presentadas al cliente.
- Funcionalidades aceptadas o rechazadas.
- Retroalimentación del cliente.
- Nuevas solicitudes.
- Lecciones aprendidas por el equipo.

### Resultado obtenido

#### Evaluación de las funcionalidades

| Funcionalidad | Evaluación del cliente | Estado |
|---|---|---|
| Registro de usuarios | El proceso es sencillo y valida correctamente los datos. | Aceptada |
| Inicio y cierre de sesión | El acceso funciona correctamente. | Aceptada |
| Creación de envíos | Permite registrar la información necesaria. | Aceptada con observaciones |
| Generación del código de seguimiento | El código se genera correctamente para cada envío. | Aceptada |
| Consulta del estado del envío | La información es correcta, pero podría ser más detallada. | Aceptada con observaciones |
| Validación de formularios | Evita el envío de datos incompletos o incorrectos. | Aceptada |

#### Retroalimentación del cliente

- Agregar las fechas estimadas de entrega a los envíos.
- Mostrar un historial con los cambios de estado del envío.
- Mejorar la visualización de la información en dispositivos móviles.
- Enviar notificaciones al cliente cuando cambie el estado de su envío.

#### Nuevas solicitudes

| ID | Nueva historia de usuario | Prioridad propuesta |
|---|---|---|
| HU07 | Como cliente, quiero consultar la fecha estimada de entrega para saber cuándo llegará mi envío. | Alta |
| HU08 | Como cliente, quiero visualizar el historial de estados para conocer el recorrido de mi envío. | Media |
| HU09 | Como cliente, quiero recibir notificaciones cuando cambie el estado de mi envío. | Alta |
| HU10 | Como usuario, quiero utilizar la aplicación desde un dispositivo móvil sin dificultades. | Media |

#### Lecciones aprendidas

- Incluir al cliente con mayor frecuencia durante el desarrollo para validar las funcionalidades.
- Definir con más detalle los datos que deben mostrarse en el seguimiento.
- Incorporar pruebas específicas para dispositivos móviles.
- Mantener actualizado el Product Backlog con la retroalimentación recibida.

### Técnicas utilizadas

- Asignación del rol de Product Owner.
- Encadenamiento mediante el incremento obtenido en el Prompt 3.
- Simulación de la reunión de revisión.
- Clasificación de funcionalidades por estado de aceptación.
- Conversión de solicitudes en nuevas historias de usuario.
- Priorización de la retroalimentación.
- Presentación estructurada mediante tablas.

## Prompt 5: Retrospectiva del Sprint

### Actividad Scrum

Durante la retrospectiva, el equipo analiza cómo se desarrolló el Sprint, identifica los aspectos positivos, los problemas encontrados y define acciones de mejora para el siguiente Sprint.

### Prompt

**Contexto:**  
Eres el Scrum Master de un equipo que desarrolla una aplicación web para una empresa de logística. Luego de realizar la revisión del Sprint, debes coordinar una retrospectiva utilizando la retroalimentación del cliente y las lecciones aprendidas.

**Instrucción:**  
Analiza la siguiente retroalimentación y simula una retrospectiva del Sprint. Identifica qué funcionó bien, qué aspectos deben mejorar y qué acciones realizará el equipo en el próximo Sprint. Asigna responsables y prioridades a cada acción.

**Entrada:**

**Retroalimentación del cliente:**

- Agregar fechas estimadas de entrega.
- Mostrar un historial con los cambios de estado del envío.
- Mejorar la visualización en dispositivos móviles.
- Enviar notificaciones cuando cambie el estado de un envío.

**Lecciones aprendidas:**

- Incluir al cliente con mayor frecuencia durante el desarrollo.
- Definir con más detalle los datos mostrados en el seguimiento.
- Incorporar pruebas específicas para dispositivos móviles.
- Mantener actualizado el Product Backlog con la retroalimentación recibida.

**Salida esperada:**

- Aspectos que funcionaron correctamente.
- Problemas y oportunidades de mejora.
- Acciones concretas para el próximo Sprint.
- Responsables de cada acción.
- Prioridad de las mejoras.
- Plan de mejora final.

### Resultado obtenido

#### Aspectos positivos

- Se completaron todas las tareas planificadas.
- Las funcionalidades principales fueron aceptadas por el cliente.
- Se corrigieron los errores encontrados durante las pruebas.
- El equipo cumplió el objetivo definido para el Sprint.
- La comunicación entre los integrantes permitió resolver los problemas detectados.

#### Aspectos por mejorar

- La participación del cliente durante el desarrollo fue limitada.
- Algunos requisitos de seguimiento no estaban suficientemente detallados.
- No se realizaron suficientes pruebas en dispositivos móviles.
- La retroalimentación del cliente no se incorporó inmediatamente al Product Backlog.
- Se deben mejorar las estimaciones y la asignación de tareas.

#### Plan de mejora para el próximo Sprint

| ID | Acción de mejora | Responsable | Prioridad |
|---|---|---|---|
| AM01 | Realizar una reunión intermedia con el cliente para validar los avances. | Product Owner | Alta |
| AM02 | Definir criterios de aceptación más detallados para cada historia. | Product Owner y equipo | Alta |
| AM03 | Incorporar pruebas funcionales en diferentes dispositivos móviles. | Tester QA | Alta |
| AM04 | Actualizar el Product Backlog después de cada reunión con el cliente. | Product Owner | Alta |
| AM05 | Revisar la estimación y distribución de tareas antes de comenzar el Sprint. | Scrum Master y equipo | Media |
| AM06 | Implementar las notificaciones por cambios de estado solicitadas por el cliente. | Desarrollador A | Alta |
| AM07 | Incorporar la fecha estimada y el historial de estados de los envíos. | Desarrolladores B y C | Media |

#### Compromiso del equipo

En el próximo Sprint, el equipo se compromete a mantener una comunicación más frecuente con el cliente, mejorar la definición de las historias de usuario y ampliar las pruebas en dispositivos móviles.

También se priorizarán las notificaciones sobre cambios de estado y la fecha estimada de entrega, debido a que fueron las solicitudes más importantes realizadas durante la revisión.

### Técnicas utilizadas

- Asignación del rol de Scrum Master.
- Encadenamiento con los resultados del Prompt 4.
- Técnica de retrospectiva: qué funcionó bien, qué debe mejorar y qué acciones realizar.
- Transformación de observaciones en acciones concretas.
- Asignación de responsables y prioridades.
- Elaboración de un plan de mejora estructurado.
