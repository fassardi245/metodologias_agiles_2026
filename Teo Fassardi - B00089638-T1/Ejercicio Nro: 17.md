# Ejercicio 17

# Consigna

Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura. La aplicación debe cumplir con los siguientes requisitos funcionales:

1. Gestión de cuentas bancarias

Permitir la creación y edición de cuentas bancarias.

Visualizar el saldo actual y el historial de movimientos de cada cuenta.

Realizar transferencias entre cuentas propias.

Descargar el historial de movimientos en formato CSV o PDF.

2. Gestión de ingresos y gastos

Permitir la creación y edición de ingresos y gastos.

Categorizar los ingresos y gastos por tipo, por ejemplo: salario, alquiler, alimentación, etc.

Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.

Establecer presupuestos para diferentes categorías de gastos.

3. Gestión de deudas

Permitir la creación y edición de deudas.

Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.

Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.

Generar informes sobre el progreso en el pago de las deudas.

Resolver
Estimación del tamaño del proyecto

Utilizando el método COSMIC, se estima que el tamaño funcional total del proyecto es de X Puntos de Función COSMIC (PFC).

Cálculo del costo por punto de función

El costo por punto de función (CPFC) se estima en Y USD.

Cantidad de puntos de función que se pueden hacer en un mes

Se estima que un equipo de desarrollo de software de Z personas puede desarrollar W Puntos de Función COSMIC (PFC) por mes.

Duración del proyecto

La duración del proyecto se estima en A meses.

Costo del proyecto

El costo total del proyecto se estima en B USD.

Instrucciones para el alumno
Identificar las interacciones funcionales: analice los requisitos funcionales descritos anteriormente e identifique todas las interacciones entre los usuarios y la aplicación.
Clasificar las interacciones funcionales: clasifique cada interacción funcional en una de las tres categorías de tamaño COSMIC: pequeña (S), mediana (M) o grande (L).
Calcular el tamaño funcional: asigne un valor de Puntos de Función COSMIC (PFC) a cada interacción funcional en función de su clasificación de tamaño y sume los valores de PFC de todas las interacciones para obtener el tamaño funcional total del proyecto en PFC.
Obtener el costo por punto de función: investigue el costo promedio de desarrollo de software en su región y considere la complejidad del proyecto para estimar el costo por punto de función (CPFC).
Determinar la cantidad de PFC por mes: estime la cantidad de Puntos de Función COSMIC (PFC) que un equipo de desarrollo de software de tamaño Z puede desarrollar por mes (W PFC/mes) en función de su experiencia y eficiencia.
Calcular la duración del proyecto: divida el tamaño funcional total del proyecto (X PFC) por la cantidad de PFC que se pueden desarrollar por mes (W PFC/mes) para obtener la duración estimada del proyecto en meses (A meses).
Estimar el costo total: multiplique el tamaño funcional total del proyecto (X PFC) por el costo por punto de función (Y USD/PFC) para obtener el costo total estimado del proyecto (B USD).

# Resolución 

## Software a desarrollar

El software a desarrollar será una aplicación web para la gestión de finanzas personales. Esta aplicación permitirá a los usuarios administrar cuentas bancarias, registrar ingresos y gastos, controlar deudas, consultar reportes financieros y descargar información en formatos como CSV o PDF.

El sistema estará compuesto por tres módulos principales: gestión de cuentas bancarias, gestión de ingresos y gastos, y gestión de deudas. A partir de estos requisitos funcionales se realiza la estimación del tamaño, duración y costo del proyecto mediante el método COSMIC.

## 1. Identificación y medición de interacciones funcionales

1. Crear cuenta bancaria.
   Movimientos COSMIC considerados: Entrada + Escritura + Salida.
   PFC: 3.
   Clasificación: Pequeña.

2. Editar cuenta bancaria.
   Movimientos COSMIC considerados: Entrada + Lectura + Entrada + Escritura + Salida.
   PFC: 5.
   Clasificación: Mediana.

3. Consultar saldo e historial de movimientos.
   Movimientos COSMIC considerados: Entrada + Lectura de cuenta + Lectura de movimientos + Salida.
   PFC: 4.
   Clasificación: Mediana.

4. Transferir dinero entre cuentas propias.
   Movimientos COSMIC considerados: Entrada + Lectura + Escritura de cuenta origen + Escritura de cuenta destino + Escritura de movimiento + Salida.
   PFC: 6.
   Clasificación: Grande.

5. Descargar historial en CSV o PDF.
   Movimientos COSMIC considerados: Entrada + Lectura + Salida.
   PFC: 3.
   Clasificación: Pequeña.

6. Crear ingreso o gasto.
   Movimientos COSMIC considerados: Entrada + Escritura + Salida.
   PFC: 3.
   Clasificación: Pequeña.

7. Editar ingreso o gasto.
   Movimientos COSMIC considerados: Entrada + Lectura + Entrada + Escritura + Salida.
   PFC: 5.
   Clasificación: Mediana.

8. Categorizar ingresos y gastos.
   Movimientos COSMIC considerados: Entrada + Lectura + Escritura + Salida.
   PFC: 4.
   Clasificación: Mediana.

9. Visualizar gráficos y reportes.
   Movimientos COSMIC considerados: Entrada + Lectura de datos + Lectura de categorías + Salida.
   PFC: 4.
   Clasificación: Mediana.

10. Establecer presupuestos por categoría.
    Movimientos COSMIC considerados: Entrada + Lectura + Escritura + Salida.
    PFC: 4.
    Clasificación: Mediana.

11. Crear deuda.
    Movimientos COSMIC considerados: Entrada + Escritura + Salida.
    PFC: 3.
    Clasificación: Pequeña.

12. Editar deuda.
    Movimientos COSMIC considerados: Entrada + Lectura + Entrada + Escritura + Salida.
    PFC: 5.
    Clasificación: Mediana.

13. Ver calendario de pagos y simulaciones.
    Movimientos COSMIC considerados: Entrada + Lectura de deuda + Lectura de pagos + Salida.
    PFC: 4.
    Clasificación: Mediana.

14. Generar informe de progreso de deudas.
    Movimientos COSMIC considerados: Entrada + Lectura de deuda + Lectura de pagos + Salida.
    PFC: 4.
    Clasificación: Mediana.

## 2. Tamaño funcional total del proyecto

Se suman todos los Puntos de Función COSMIC obtenidos en las interacciones funcionales identificadas:

3 + 5 + 4 + 6 + 3 + 3 + 5 + 4 + 4 + 4 + 3 + 5 + 4 + 4 = 57 PFC

Por lo tanto:

X = 57 Puntos de Función COSMIC.

El tamaño funcional total estimado del proyecto es de 57 PFC.

## 3. Cálculo del costo por punto de función

Para calcular el costo por punto de función, se toma como base el costo mensual estimado del equipo de trabajo definido para este proyecto.

El equipo estará compuesto por 4 personas:

2 desarrolladores: 2.500 USD cada uno = 5.000 USD.
1 QA / tester: 2.000 USD.
1 líder técnico o analista funcional: 3.500 USD.
Gastos administrativos e infraestructura: 1.500 USD.

Costo mensual total del equipo:

5.000 USD + 2.000 USD + 3.500 USD + 1.500 USD = 12.000 USD.

Productividad mensual estimada:

W = 23 PFC por mes.

La fórmula utilizada es:

Costo por punto de función = Costo mensual del equipo / PFC desarrollados por mes

Aplicando los valores:

Y = 12.000 USD / 23 PFC

Y = 521,74 USD/PFC

Por lo tanto, el costo estimado por punto de función para este proyecto es de 521,74 USD/PFC.

## 4. Cantidad de puntos de función que se pueden hacer en un mes

Se estima un equipo de desarrollo de software de 4 personas.

Z = 4 personas.

El equipo propuesto estaría compuesto por:

2 desarrolladores.
1 QA / tester.
1 líder técnico o analista funcional.

La productividad mensual estimada del equipo es:

W = 23 PFC por mes.

Esto significa que el equipo podría desarrollar aproximadamente 23 Puntos de Función COSMIC por mes.

## 5. Duración del proyecto

La fórmula para calcular la duración del proyecto es:

Duración = Tamaño funcional total / PFC por mes

Aplicando los valores:

A = 57 / 23

A = 2,48 meses

Duración estimada: 2 meses y medio (aprox 75 dias).

Por lo tanto, la duración aproximada del proyecto será de 3 meses.

## 6. Costo total del proyecto

La fórmula para calcular el costo total del proyecto es:

Costo total = Tamaño funcional total × Costo por punto de función

Aplicando los valores:

B = 57 × 521,74 USD

B = 29.739,18 USD

Por lo tanto, el costo total estimado del proyecto es de 29.739,18 USD.

## Resultado final

Estimación del tamaño del proyecto:

Utilizando el método COSMIC, se estima que el tamaño funcional total del proyecto es de 57 Puntos de Función COSMIC (PFC).

Cálculo del costo por punto de función:

El costo por punto de función se estima en 521,74 USD/PFC.

Cantidad de puntos de función que se pueden hacer en un mes:

Se estima que un equipo de desarrollo de software de 4 personas puede desarrollar 23 PFC por mes.

Duración del proyecto:

La duración del proyecto es de 2 meses y medio (aprox 75 dias).

Costo del proyecto:

El costo total estimado del proyecto es de 29.739,18 USD.

