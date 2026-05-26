## Ejercicio Nro: 13
# Enunciado
Tu tarea es desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir a los usuarios abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas. A continuación se detallan las etapas de desarrollo utilizando TDD:

Etapa 1: Especificación y prueba inicial

Especifica los requisitos básicos del sistema y las funcionalidades clave, como la apertura de cuenta, depósito de fondos, retiro de fondos y transferencia de fondos.
Escribe una prueba inicial que verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial.
Etapa 2: Desarrollo de las funcionalidades básicas

Implementa la funcionalidad para abrir una cuenta bancaria, asegurándote de que se cumplan los requisitos especificados. Ejecuta la prueba y verifica que pase correctamente.
Implementa la funcionalidad para realizar depósitos en una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
Implementa la funcionalidad para realizar retiros de una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
Implementa la funcionalidad para transferir fondos entre cuentas bancarias. Ejecuta las pruebas y verifica que pasen correctamente.
Etapa 3: Pruebas adicionales y mejoras

Escribe pruebas adicionales para cubrir casos de prueba específicos, como intentar retirar más dinero del disponible en una cuenta o transferir fondos a una cuenta inexistente.
Ejecuta todas las pruebas y verifica que pasen correctamente.
Refactoriza tu código si es necesario para mejorar su estructura, legibilidad y eficiencia.
Ejecuta todas las pruebas nuevamente para asegurarte de que el código refactorizado no haya introducido errores.
Etapa 4: Cobertura completa de pruebas

Asegúrate de que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas.
Examina los casos límite y situaciones excepcionales para garantizar que el sistema se comporte correctamente en todos los escenarios.
Ejecuta todas las pruebas y verifica que pasen correctamente.
Recuerda seguir el enfoque TDD, donde agregarás una prueba antes de implementar cada funcionalidad y verificarás que todas las pruebas pasen antes de pasar a la siguiente etapa. Esto te ayudará a desarrollar una aplicación confiable, mantenible y que cumpla con los requisitos establecidos.

# Resolución

1. Especificación de los requisitos básicos del sistema
El sistema a desarrollar corresponde a una aplicación bancaria simple. Su objetivo es permitir la gestión básica de cuentas bancarias mediante operaciones comunes.
Las funcionalidades principales son:
•	crear o abrir una cuenta bancaria; 
•	consultar el saldo disponible; 
•	realizar depósitos; 
•	realizar retiros; 
•	transferir fondos entre cuentas; 
•	validar operaciones incorrectas. 
Cada cuenta bancaria debe contar con un titular, un número identificador de cuenta y un saldo. Además, el sistema debe controlar que las operaciones respeten reglas básicas, por ejemplo que no se depositen montos negativos, que no se retire más dinero del disponible y que no se transfiera dinero a cuentas inexistentes.

2. Prueba inicial para crear una cuenta y consultar saldo
Siguiendo el enfoque TDD, antes de implementar la funcionalidad se plantea una primera prueba.
La primera prueba consiste en verificar que el sistema pueda crear una cuenta bancaria nueva y consultar correctamente su saldo inicial.
Por ejemplo, si se abre una cuenta con saldo inicial igual a cero, el resultado esperado es que el sistema permita crear la cuenta y que al consultar el saldo devuelva cero.
Esta prueba es importante porque permite comprobar que existe una estructura básica de cuenta bancaria antes de avanzar con operaciones más complejas.
Resultado esperado:
la cuenta se crea correctamente y el saldo inicial coincide con el valor definido.

3. Implementación de la apertura de cuenta bancaria
Luego de definir la prueba inicial, se implementa la funcionalidad mínima necesaria para abrir una cuenta bancaria.
La cuenta debe crearse con datos básicos:
•	titular; 
•	número de cuenta; 
•	saldo inicial. 
También deben agregarse validaciones. Por ejemplo, el sistema no debería permitir crear una cuenta sin titular o con saldo inicial negativo.
Después de implementar esta funcionalidad, se ejecuta la prueba planteada en la consigna anterior. Si la prueba pasa, significa que la apertura de cuenta funciona correctamente.
Resultado esperado:
el sistema permite abrir cuentas válidas y rechaza cuentas con datos incorrectos.

4. Implementación de depósitos en una cuenta bancaria
La siguiente funcionalidad consiste en permitir que el usuario deposite dinero en una cuenta.
Primero se plantea la prueba. Por ejemplo: una cuenta tiene saldo inicial de $0 y se realiza un depósito de $1000. El resultado esperado es que el saldo final sea $1000.
Luego se implementa la operación de depósito.
También se deben contemplar casos inválidos. El sistema no debería permitir depósitos con monto cero o con valores negativos, porque eso no representa una operación bancaria válida.
Resultado esperado:
el depósito aumenta correctamente el saldo de la cuenta y el sistema rechaza montos inválidos.

5. Implementación de retiros en una cuenta bancaria
Después se desarrolla la funcionalidad de retiro de fondos.
Primero se define una prueba. Por ejemplo: una cuenta tiene $1000 y se retiran $400. El saldo final debería ser $600.
Luego se implementa la operación de retiro.
El sistema debe validar que el monto a retirar sea mayor que cero y que la cuenta tenga saldo suficiente. Si el usuario intenta retirar más dinero del disponible, la operación debe ser rechazada.
Resultado esperado:
el retiro descuenta correctamente el dinero del saldo, siempre que haya fondos suficientes.

6. Implementación de transferencia entre cuentas bancarias
La transferencia permite mover dinero desde una cuenta origen hacia una cuenta destino.
Primero se plantea una prueba. Por ejemplo: una cuenta origen tiene $1000 y una cuenta destino tiene $200. Si se transfieren $300, la cuenta origen debe quedar con $700 y la cuenta destino con $500.
Luego se implementa la funcionalidad de transferencia.
Esta operación debe validar que la cuenta destino exista, que el monto sea válido y que la cuenta origen tenga saldo suficiente.
Resultado esperado:
el dinero se descuenta de la cuenta origen y se acredita en la cuenta destino correctamente.

7. Pruebas adicionales para casos específicos
Una vez implementadas las operaciones principales, se agregan pruebas adicionales para verificar situaciones especiales o errores posibles.
Algunos casos importantes son:
•	intentar retirar más dinero del disponible; 
•	intentar depositar un monto negativo; 
•	intentar depositar monto cero; 
•	intentar transferir más dinero del saldo disponible; 
•	intentar transferir a una cuenta inexistente; 
•	intentar crear una cuenta sin titular; 
•	intentar crear una cuenta con saldo inicial negativo. 
Estas pruebas permiten comprobar que el sistema no solo funciona en casos normales, sino también frente a situaciones incorrectas.
Resultado esperado:
el sistema debe rechazar las operaciones inválidas y conservar correctamente los saldos de las cuentas.

8. Ejecución de todas las pruebas
Después de agregar las pruebas principales y adicionales, se ejecuta el conjunto completo de pruebas.
El objetivo es verificar que todas las funcionalidades implementadas funcionen correctamente y que ninguna modificación haya afectado operaciones anteriores.
En TDD, no se debería avanzar a una nueva funcionalidad si las pruebas anteriores no pasan correctamente.
Resultado esperado:
todas las pruebas deben pasar antes de continuar con nuevas mejoras o cambios.

9. Refactorización del código
Cuando las pruebas ya pasan, se revisa el código para mejorar su estructura interna.
La refactorización no busca agregar nuevas funcionalidades, sino mejorar la calidad del código existente.
Algunas mejoras posibles son:
•	mejorar nombres de variables y métodos; 
•	evitar código repetido; 
•	ordenar las validaciones; 
•	separar responsabilidades; 
•	simplificar operaciones; 
•	hacer el código más claro y fácil de mantener. 
Por ejemplo, la transferencia puede aprovechar las operaciones de retiro y depósito ya existentes, en lugar de repetir la lógica de descontar y sumar saldo.
Resultado esperado:
el código queda más claro y mantenible, pero el comportamiento del sistema sigue siendo el mismo.

10. Nueva ejecución de pruebas después de refactorizar
Luego de refactorizar, se deben ejecutar nuevamente todas las pruebas.
Esto es fundamental porque permite comprobar que las mejoras internas no hayan introducido errores.
Si todas las pruebas siguen pasando, significa que el código fue mejorado sin modificar el comportamiento esperado del sistema.
Resultado esperado:
todas las pruebas deben pasar igual que antes de la refactorización.

11. Cobertura de todas las funcionalidades con pruebas automatizadas
En esta etapa se revisa que cada funcionalidad importante del sistema tenga al menos una prueba automatizada.
Deben estar cubiertas las siguientes operaciones:
•	apertura de cuenta; 
•	consulta de saldo; 
•	depósito de fondos; 
•	retiro de fondos; 
•	transferencia entre cuentas; 
•	validación de errores; 
•	casos límite. 
Esto permite tener mayor seguridad ante cambios futuros. Si más adelante se modifica alguna parte del sistema, las pruebas ayudarán a detectar rápidamente si algo dejó de funcionar.
Resultado esperado:
todas las funcionalidades principales quedan respaldadas por pruebas.

12. Revisión de casos límite y situaciones excepcionales
Además de probar los casos normales, también deben revisarse los casos límite.
Algunos ejemplos son:
•	saldo inicial igual a cero; 
•	saldo inicial negativo; 
•	depósito de monto cero; 
•	retiro de monto cero; 
•	transferencia de monto cero; 
•	retiro sin fondos suficientes; 
•	transferencia hacia una cuenta inexistente; 
•	cuenta sin titular; 
•	cuenta sin número identificador. 
Estos casos son importantes porque muchas fallas aparecen justamente en situaciones no habituales.
Resultado esperado:
el sistema debe comportarse correctamente tanto en operaciones normales como en casos excepcionales.

13. Ejecución final de todas las pruebas
Por último, se ejecutan nuevamente todas las pruebas del sistema.
Esta ejecución final permite comprobar que la aplicación cumple con los requisitos definidos y que las operaciones bancarias funcionan correctamente.
Si todas las pruebas pasan, se puede considerar que el sistema está en una versión estable.
Resultado esperado:
la aplicación permite abrir cuentas, consultar saldos, depositar, retirar y transferir fondos, validando correctamente las operaciones inválidas.
