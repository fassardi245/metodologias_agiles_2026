# Ejercicio N.º 13

## Enunciado

Desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas.

### Etapa 1: Especificación y prueba inicial

- Especificar los requisitos básicos y las funcionalidades principales.
- Escribir una prueba inicial que verifique la creación de una cuenta bancaria y su saldo inicial.

### Etapa 2: Desarrollo de las funcionalidades básicas

- Implementar la apertura de una cuenta bancaria.
- Implementar depósitos.
- Implementar retiros.
- Implementar transferencias entre cuentas.
- Ejecutar las pruebas después de cada implementación.

### Etapa 3: Pruebas adicionales y mejoras

- Agregar pruebas para casos específicos, como retirar más dinero del disponible o transferir a una cuenta inexistente.
- Ejecutar todas las pruebas.
- Refactorizar el código para mejorar su estructura y legibilidad.
- Ejecutar nuevamente las pruebas.

### Etapa 4: Cobertura completa de pruebas

- Cubrir todas las funcionalidades mediante pruebas automatizadas.
- Examinar casos límite y situaciones excepcionales.
- Ejecutar todas las pruebas y verificar que sean aprobadas.

El trabajo debe seguir el enfoque TDD: escribir una prueba antes de implementar cada funcionalidad y comprobar que todas las pruebas pasen antes de continuar.

# Resolución

## Etapa 1: Especificación y prueba inicial

### Requisitos básicos del sistema

El sistema corresponde a una aplicación bancaria simple. Su objetivo es permitir la gestión básica de cuentas bancarias mediante las siguientes operaciones:

- Crear o abrir una cuenta bancaria.
- Consultar el saldo disponible.
- Realizar depósitos.
- Realizar retiros.
- Transferir fondos entre cuentas.
- Validar operaciones incorrectas.

Cada cuenta bancaria debe contar con un titular, un número identificador y un saldo.

El sistema también debe impedir depósitos negativos, retiros superiores al saldo disponible y transferencias hacia cuentas inexistentes.

### Prueba inicial para crear una cuenta y consultar su saldo — Ciclo RED

Antes de implementar la funcionalidad, se escribe una prueba que verifica que el sistema pueda crear una cuenta bancaria y consultar su saldo inicial.

La prueba fallará inicialmente porque la clase todavía no existe.

```javascript
// cuentaBancaria.test.js

const { CuentaBancaria } = require("./cuentaBancaria");

describe("Etapa 1: Creación de cuenta", () => {
  test("Debería crear una cuenta con titular, número y saldo inicial en 0", () => {
    const cuenta = new CuentaBancaria("Juan Pérez", "123456");

    expect(cuenta.getTitular()).toBe("Juan Pérez");
    expect(cuenta.getNumeroCuenta()).toBe("123456");
    expect(cuenta.getSaldo()).toBe(0);
  });
});
```

## Etapa 2: Desarrollo de las funcionalidades básicas

### Apertura de una cuenta bancaria — Ciclo GREEN

Se implementa la funcionalidad mínima necesaria para abrir una cuenta con titular, número identificador y saldo inicial igual a cero.

```javascript
// cuentaBancaria.js

class CuentaBancaria {
  constructor(titular, numeroCuenta) {
    if (!titular || !numeroCuenta) {
      throw new Error("Datos obligatorios faltantes");
    }

    this.titular = titular;
    this.numeroCuenta = numeroCuenta;
    this.saldo = 0;
  }

  getTitular() {
    return this.titular;
  }

  getNumeroCuenta() {
    return this.numeroCuenta;
  }

  getSaldo() {
    return this.saldo;
  }
}

module.exports = { CuentaBancaria };
```

Después de implementar esta funcionalidad, se ejecuta la prueba inicial para comprobar que sea aprobada.

### Implementación de depósitos

Primero se escribe una prueba para comprobar que un depósito válido incremente el saldo.

```javascript
test("Debería incrementar el saldo al realizar un depósito válido", () => {
  const cuenta = new CuentaBancaria("Juan Pérez", "123456");

  cuenta.depositar(1000);

  expect(cuenta.getSaldo()).toBe(1000);
});
```

Luego se implementa el método correspondiente:

```javascript
depositar(monto) {
  if (monto <= 0) {
    throw new Error("El monto a depositar debe ser mayor a cero");
  }

  this.saldo += monto;
}
```

### Implementación de retiros

Primero se define una prueba en la que una cuenta tiene `$1000` y se retiran `$400`. El saldo final debe ser de `$600`.

```javascript
test("Debería disminuir el saldo al realizar un retiro válido", () => {
  const cuenta = new CuentaBancaria("Juan Pérez", "123456");

  cuenta.depositar(1000);
  cuenta.retirar(400);

  expect(cuenta.getSaldo()).toBe(600);
});
```

Luego se implementa la operación:

```javascript
retirar(monto) {
  if (monto <= 0) {
    throw new Error("El monto a retirar debe ser mayor a cero");
  }

  if (monto > this.saldo) {
    throw new Error("Fondos insuficientes");
  }

  this.saldo -= monto;
}
```

### Implementación de transferencias

La transferencia permite mover dinero desde una cuenta de origen hacia una cuenta de destino.

Primero se escribe la prueba correspondiente:

```javascript
test("Debería transferir fondos correctamente entre dos cuentas", () => {
  const cuentaOrigen = new CuentaBancaria("Juan Pérez", "123456");
  const cuentaDestino = new CuentaBancaria("María López", "789101");

  cuentaOrigen.depositar(1000);
  cuentaOrigen.transferir(300, cuentaDestino);

  expect(cuentaOrigen.getSaldo()).toBe(700);
  expect(cuentaDestino.getSaldo()).toBe(300);
});
```

Luego se implementa la lógica básica:

```javascript
transferir(monto, cuentaDestino) {
  if (!cuentaDestino) {
    throw new Error("La cuenta destino no existe");
  }

  if (monto > this.saldo) {
    throw new Error("Fondos insuficientes para transferir");
  }

  this.saldo -= monto;
  cuentaDestino.saldo += monto;
}
```

## Etapa 3: Pruebas adicionales y mejoras

### Pruebas para casos específicos

Se agregan pruebas para verificar el comportamiento del sistema ante errores o entradas inválidas.

```javascript
describe("Etapa 3: Casos de error y límites", () => {
  let cuenta;

  beforeEach(() => {
    cuenta = new CuentaBancaria("Juan Pérez", "123456");
  });

  test("No debería permitir retirar más dinero del disponible", () => {
    cuenta.depositar(100);

    expect(() => cuenta.retirar(150)).toThrow(
      "Fondos insuficientes"
    );
  });

  test("No debería permitir depósitos negativos o iguales a cero", () => {
    expect(() => cuenta.depositar(-50)).toThrow(
      "El monto a depositar debe ser mayor a cero"
    );

    expect(() => cuenta.depositar(0)).toThrow(
      "El monto a depositar debe ser mayor a cero"
    );
  });

  test("No debería permitir transferencias a cuentas inexistentes", () => {
    cuenta.depositar(500);

    expect(() => cuenta.transferir(200, null)).toThrow(
      "La cuenta destino no existe"
    );
  });
});
```

### Ejecución de todas las pruebas

Se ejecuta la suite completa para comprobar que las pruebas iniciales y adicionales sean aprobadas antes de modificar la estructura del código.

### Refactorización del código — Ciclo REFACTOR

Con las pruebas aprobadas, se mejora el método `transferir` para reutilizar los métodos `retirar` y `depositar`. De esta manera se evita duplicar la lógica de negocio.

```javascript
// cuentaBancaria.js

class CuentaBancaria {
  constructor(titular, numeroCuenta) {
    if (!titular || !numeroCuenta) {
      throw new Error("Datos obligatorios faltantes");
    }

    this.titular = titular;
    this.numeroCuenta = numeroCuenta;
    this.saldo = 0;
  }

  getTitular() {
    return this.titular;
  }

  getNumeroCuenta() {
    return this.numeroCuenta;
  }

  getSaldo() {
    return this.saldo;
  }

  depositar(monto) {
    if (monto <= 0) {
      throw new Error("El monto a depositar debe ser mayor a cero");
    }

    this.saldo += monto;
  }

  retirar(monto) {
    if (monto <= 0) {
      throw new Error("El monto a retirar debe ser mayor a cero");
    }

    if (monto > this.saldo) {
      throw new Error("Fondos insuficientes");
    }

    this.saldo -= monto;
  }

  transferir(monto, cuentaDestino) {
    if (!cuentaDestino) {
      throw new Error("La cuenta destino no existe");
    }

    this.retirar(monto);
    cuentaDestino.depositar(monto);
  }
}

module.exports = { CuentaBancaria };
```

### Nueva ejecución después de refactorizar

Se ejecuta nuevamente toda la suite de pruebas para confirmar que la refactorización no haya introducido errores ni modificado el comportamiento del sistema.

## Etapa 4: Cobertura completa de pruebas

### Cobertura de las funcionalidades

Se verifica que las siguientes funcionalidades estén cubiertas por pruebas automatizadas:

- Apertura de una cuenta.
- Consulta del saldo.
- Depósitos.
- Retiros.
- Transferencias.
- Validación de fondos insuficientes.
- Validación de montos incorrectos.
- Validación de cuentas inexistentes.

### Casos límite y situaciones excepcionales

También se analiza el comportamiento del sistema ante situaciones como:

- Crear una cuenta sin titular.
- Crear una cuenta sin número identificador.
- Retirar todo el saldo disponible.
- Transferir todo el saldo disponible.
- Realizar operaciones con montos iguales a cero.
- Realizar operaciones con montos negativos.

### Ejecución final

Como cierre del proceso TDD, se ejecuta por última vez la suite completa de pruebas automatizadas.

Al aprobarse todas las pruebas, se confirma que la aplicación cumple con los requisitos definidos y que la refactorización no introdujo errores.
