# Ejercicio Nro. 12.2: Metodología Lean con Odoo Project

## Consigna

Aplicar los principios de Lean Development en la empresa ficticia LeanDev, utilizando Odoo Project para configurar un proyecto, crear un tablero Kanban, organizar tareas, establecer límites de trabajo en curso, detectar desperdicios y aplicar mejoras continuas.

También se deberán resolver cinco casos relacionados con problemas frecuentes en proyectos de software y documentar las prácticas Lean aplicadas.

## Resolución

Para realizar la actividad se propone el desarrollo de un sistema web de gestión de pedidos para una pyme. El sistema permitirá registrar clientes, cargar pedidos, consultar su estado y confirmar entregas.

## Parte 1: Diagnóstico inicial del proceso

Se analizó el proceso de trabajo de LeanDev y se detectaron los siguientes desperdicios:

| Desperdicio | Situación detectada | Consecuencia |
|---|---|---|
| Espera | Las tareas permanecen varios días esperando ser probadas. | Demoras en las entregas |
| Sobreproducción | Se desarrollan funciones que el cliente no solicitó. | Uso innecesario de tiempo |
| Retrabajo | Algunas tareas regresan a desarrollo por requisitos poco claros. | Aumento de costos |
| Trabajo en curso excesivo | Los desarrolladores comienzan varias tareas simultáneamente. | Pocas tareas terminadas |
| Defectos | Los errores son detectados después de la publicación. | Reclamos del cliente |

En Odoo se deberá crear una tarea llamada **Diagnóstico inicial del proceso**, incluyendo estos cinco desperdicios y sus consecuencias.

## Parte 2: Propuesta de valor y etapas

### Producto Mínimo Viable

El MVP incluirá únicamente las funciones necesarias para que la pyme pueda administrar sus pedidos:

- Registro e inicio de sesión.
- Registro de clientes.
- Creación de pedidos.
- Consulta del estado de los pedidos.
- Confirmación de entregas.

Las funciones de reportes avanzados, notificaciones automáticas y estadísticas quedarán para futuras versiones.

### Flujo Kanban

El tablero de Odoo tendrá las siguientes etapas:

1. Backlog.
2. Revisión de requisitos.
3. Listo para desarrollar.
4. En desarrollo.
5. Revisión de código.
6. Testing.
7. Demo con cliente.
8. Finalizado.

### Límites WIP

| Etapa | Límite WIP | Justificación |
|---|---:|---|
| Revisión de requisitos | 3 tareas | Evitar acumulación de requisitos sin validar |
| En desarrollo | 4 tareas | Permitir que el equipo se concentre en terminar |
| Revisión de código | 2 tareas | Mantener una revisión ordenada |
| Testing | 2 tareas | Evitar sobrecargar al responsable de pruebas |
| Demo con cliente | 2 tareas | Obtener validaciones frecuentes |

Cuando una etapa alcance su límite, el equipo deberá ayudar a terminar las tareas existentes antes de comenzar otras.

## Parte 3: Priorización y visualización

El Product Backlog se organizará mediante prioridades y etiquetas.

| Tarea | Etiqueta | Prioridad |
|---|---|---|
| Registro de usuarios | Feature | Alta |
| Registro de clientes | Feature | Alta |
| Creación de pedidos | Feature | Alta |
| Consulta del estado | Feature | Alta |
| Corrección de pedidos duplicados | Bug | Alta |
| Mejorar formulario de pedidos | Improvement | Media |
| Notificaciones automáticas | Feature | Baja |
| Reportes mensuales | Feature | Baja |

### Simulación de reunión diaria

| Integrante | Avance | Próxima tarea | Bloqueo |
|---|---|---|---|
| Desarrollador A | Terminó el registro de usuarios | Comenzará el registro de clientes | Ninguno |
| Desarrollador B | Avanzó con la creación de pedidos | Conectará el formulario con la base de datos | Falta confirmar un requisito |
| Tester QA | Probó el inicio de sesión | Probará el registro de clientes | Testing alcanzó su límite WIP |

Los avances y bloqueos deberán registrarse en los comentarios de las tareas correspondientes de Odoo.

## Parte 4: Mejora continua

### Cuello de botella identificado

Se detectó una acumulación de tareas en Testing debido a que ingresan más tareas de las que el responsable puede validar. Esto retrasa las entregas y aumenta el trabajo pendiente.

### Aplicación del ciclo PDCA

| Etapa | Acción |
|---|---|
| Plan | Limitar Testing a dos tareas y definir criterios de aceptación antes del desarrollo |
| Do | Aplicar el límite durante el siguiente ciclo y solicitar apoyo de un desarrollador |
| Check | Comparar el tiempo de espera y la cantidad de tareas terminadas |
| Act | Mantener la medida si reduce las demoras o ajustar el límite si fuera necesario |

### Retrospectiva

**Aspectos positivos:**

- El tablero permitió visualizar el estado de las tareas.
- Las prioridades ayudaron a concentrarse en el MVP.
- Los límites WIP redujeron la cantidad de tareas abiertas.

**Aspectos por mejorar:**

- Validar los requisitos con mayor anticipación.
- Incorporar pruebas durante el desarrollo.
- Mejorar la distribución del trabajo.
- Registrar los bloqueos inmediatamente.

## Caso 1: Retrabajo constante en entregas

**Problema:** El cliente recibe funcionalidades que no solicitó o que no responden a sus necesidades.

**Resolución:**

- Crear la tarea **Detectar origen del retrabajo**.
- Agregar la etapa **Revisión de Requisitos**.
- Definir criterios de aceptación antes del desarrollo.
- Solicitar la aprobación del cliente o Product Owner.
- Establecer un límite WIP de tres tareas en validación.
- No permitir que una tarea avance sin requisitos aprobados.

**Resultado esperado:** Reducir devoluciones y desarrollar funcionalidades acordes con las necesidades del cliente.

## Caso 2: Bloqueo en Testing por sobrecarga

**Problema:** Existen varias tareas esperando validación y poca capacidad para probarlas.

**Resolución:**

- Registrar Testing como cuello de botella.
- Establecer un límite WIP de dos tareas.
- Aplicar la política **No iniciar nuevas tareas si Testing está lleno**.
- Solicitar apoyo temporal de un desarrollador.
- Incorporar pruebas básicas antes de enviar una tarea a Testing.

**Resultado esperado:** Disminuir la acumulación de tareas y acelerar las validaciones.

## Caso 3: Bugs recurrentes después de producción

**Problema:** Muchos errores se detectan luego de publicar las funcionalidades.

**Resolución:**

- Incorporar revisiones de código entre pares.
- Crear la tarea **Implementar tests automatizados básicos**.
- Utilizar la etiqueta **Prevención de errores**.
- Agregar criterios de prueba a cada tarea.
- No publicar una funcionalidad sin completar las pruebas.

**Resultado esperado:** Detectar los errores antes de producción y reducir reclamos.

## Caso 4: Funcionalidades no utilizadas

**Problema:** El cliente no utiliza varias de las funciones desarrolladas.

**Resolución:**

- Consultar al cliente cuáles son las funciones utilizadas.
- Identificar y registrar las funcionalidades sin uso.
- Dividir las entregas en incrementos pequeños.
- Crear la tarea **Demo con cliente** antes de cerrar cada feature.
- Utilizar la retroalimentación para decidir si una función continúa en el Backlog.

**Resultado esperado:** Evitar la sobreproducción y concentrar el trabajo en funciones que aporten valor.

## Caso 5: Saturación del equipo senior

**Problema:** Los desarrolladores senior tienen demasiadas tareas mientras los junior permanecen ociosos.

**Resolución:**

- Redistribuir tareas según dificultad y experiencia.
- Asignar tareas sencillas a los desarrolladores junior.
- Crear tareas de **Mentoría rápida**.
- Programar sesiones de apoyo y revisión de código.
- Registrar el progreso de los junior.
- Evitar que todas las decisiones dependan de una sola persona.

**Resultado esperado:** Equilibrar la carga, mejorar la autonomía de los junior y reducir el cuello de botella.

## Prácticas Lean aplicadas

- Eliminación de desperdicios.
- Desarrollo basado en un MVP.
- Visualización del trabajo mediante Kanban.
- Limitación del trabajo en curso.
- Priorización según el valor para el cliente.
- Entregas pequeñas e incrementales.
- Validación temprana de requisitos.
- Prevención de errores.
- Mejora continua mediante PDCA.
- Distribución equilibrada del conocimiento.

## Resultados observados en la simulación

La aplicación de estas medidas permitió visualizar mejor el trabajo, reducir la cantidad de tareas abiertas y detectar rápidamente los bloqueos. También mejoró la validación de requisitos, la distribución de tareas y la participación del cliente.

Los límites WIP ayudaron a evitar acumulaciones, mientras que las revisiones de código y las pruebas anticipadas permitieron prevenir errores antes de producción.

## Conclusión

La metodología Lean permitió organizar el proyecto alrededor del valor entregado al cliente. El uso de Odoo Project facilitó la visualización del flujo, la priorización de tareas y el registro de bloqueos y mejoras.

La combinación del tablero Kanban, los límites WIP, las entregas incrementales y el ciclo PDCA permitió proponer un proceso de desarrollo más ordenado y eficiente.

## Capturas de Odoo

## Capturas de Odoo

### 1. Tablero Kanban completo

Captura general donde se observan todas las etapas, las tareas distribuidas, las etiquetas, las prioridades y los límites WIP.

<img width="1918" height="660" alt="image" src="https://github.com/user-attachments/assets/b5d4af53-92b4-47e4-b943-8bf459c94977" />

### 2. Diagnóstico inicial del proceso

Captura de la tarea donde se muestran los cinco desperdicios detectados, sus consecuencias, la etiqueta Improvement y su prioridad.

<img width="1918" height="966" alt="image" src="https://github.com/user-attachments/assets/740cf70b-a839-46f9-9068-09e17c847d7a" />

### 3. Simulación de la reunión diaria y registro de bloqueos

Captura de la tarea Creación de pedidos con el avance realizado, el bloqueo detectado y el próximo paso.

<img width="1918" height="967" alt="image" src="https://github.com/user-attachments/assets/822ac1ac-ff8b-4c00-9764-246f67f19610" />

### 4. Límite WIP en Testing

Captura del tablero donde se observan dos tareas en Testing: Registro de clientes y Confirmación de entregas.

<img width="1918" height="963" alt="image" src="https://github.com/user-attachments/assets/6126f499-68f6-4218-9128-3a59dd1648d9" />

### 5. Validación temprana de requisitos

Captura de la tarea Detectar origen del retrabajo con las acciones propuestas para evitar funcionalidades incorrectas.

<img width="1918" height="967" alt="image" src="https://github.com/user-attachments/assets/e2ef6c28-83e9-49aa-a92b-28564f934631" />

### 6. Prevención de errores

Captura de la tarea Implementar tests automatizados básicos con la etiqueta Prevención de errores y las acciones definidas.

<img width="1918" height="968" alt="image" src="https://github.com/user-attachments/assets/5f55b970-3ca1-4757-86dc-050f6f99ad4b" />

### 7. Funcionalidades no utilizadas

Captura de la tarea Identificar funcionalidades no utilizadas con las medidas para evitar la sobreproducción.

<img width="1918" height="965" alt="image" src="https://github.com/user-attachments/assets/c6fe0277-8b04-4c0b-9aa3-27fbe9a61dd3" />

### 8. Mentoría y distribución del trabajo

Captura de la tarea Mentoría rápida con las medidas para equilibrar el trabajo entre desarrolladores senior y junior.

<img width="1918" height="967" alt="image" src="https://github.com/user-attachments/assets/02c3543f-4653-4a07-9cb3-edad076b92fc" />

### 9. Mejora continua y retrospectiva

Captura de la tarea Documentar retrospectiva con el ciclo PDCA, los aspectos positivos y los puntos por mejorar.

<img width="1918" height="968" alt="image" src="https://github.com/user-attachments/assets/dcb4b1a0-4347-4dc4-89a8-15f81d259932" />
