# javascript-fundamentals

Ejemplos desarrollados en clase sobre los fundamentos de JavaScript, la programación funcional y la programación orientada a objetos, ejecutables con Node.js.

## Datos académicos

| Campo | Detalle |
|---|---|
| **Universidad**| Universidad Autonoma de Chihuahua |
| **Facultad** | Facultad de Ingenieria |
| **Carrera** | Ingenieiía en Computacion |
| **Materia** | Desarrollo Basado en Plataformas |
| **Docente** | Mtro. Luis Antonio Ramírez Martínez |
| **Actividad** | Actividad 2. Introducción a JavaScript y sus paradigmas de programación |
| **Alumna** | Giovanna Paulina Hernández Mendoza |
| **Matrícula** | 377284 |
| **Fecha de entrega** | 15/11/2026 |

## Descripción

Colección de ejemplos desarrollados durante clase para conocer el lenguaje JavaScript y dos de sus paradigmas principales: la programación funcional y la programación orientada a objetos. Cada archivo corresponde a un subtema de la unidad, es independiente de los demás y se ejecuta con Node.js sin instalar dependencias.

## Objetivo

Comprender los fundamentos de JavaScript y aplicar los conceptos básicos de programación funcional y orientada a objetos mediante ejemplos prácticos, utilizando Git y GitHub para gestionar y publicar el código fuente.

## Tecnologías utilizadas

- JavaScript (ES6+)
- Node.js
- Git y GitHub
- Visual Studio Code / WebStorm (editor de código)

## Requisitos previos

- [Node.js](https://nodejs.org/) (versión 18 o superior recomendada)
- [Git](https://git-scm.com/)

Verifica la instalación:

```bash
node --version
git --version
```

## Instalación

El proyecto no tiene dependencias externas, por lo que basta con clonarlo:

```bash
git clone https://github.com/<usuario>/javascript-fundamentals.git
cd javascript-fundamentals
```

## Ejecución

Cada archivo se ejecuta por separado desde la terminal, dentro de la carpeta del proyecto:

```bash
node app.js
node cal.js
node poo.js
```

La salida se muestra directamente en la consola. Los nombres de archivo van en minúsculas, ya que en Linux y macOS Node distingue mayúsculas de minúsculas.

## Funcionalidades / uso

| Archivo | Subtema | Contenido |
|---|---|---|
| `app.js` | 2.2.1 Introducción a los lenguajes de scripting | Variables con `var`, `let` y `const`; tipos de datos y objetos; arreglos y listas; funciones tradicionales, anónimas y flecha; funciones como argumentos de otras funciones; enumeraciones con objetos. |
| `cal.js` | 2.2.2 Programación funcional aplicada a la web | Calculadora con multiplicación y división; composición de funciones; callbacks de éxito y error; promesas con `.then()` y `.catch()`; `async/await`. |
| `poo.js` | 2.2.3 Programación orientada a objetos aplicada a la web | Clases y constructores; creación de objetos con `new`; getters y setters; herencia con `extends` y `super`; método estático e `instanceof`; polimorfismo con una jerarquía de animales (`Animal`, `Dog`, `Cat`). |

### `app.js`: fundamentos

- **Variables:** `var` tiene alcance de función, `let` de bloque y `const` no admite reasignación (por ejemplo, `PI`).
- **Tipos de datos:** cadenas, números, booleanos, caracteres y objetos anidados (`prototype` con su `address`).
- **Arreglos:** listas de números, booleanos, caracteres y objetos.
- **Funciones:** expresiones de función, funciones anónimas y flecha, y la función `print`, que recibe otra función como argumento.
- **Enumeraciones:** el objeto `seasons` representa un enum.

Salida esperada:

```text
11
6
20
28
25
Summer
```

### `cal.js`: programación funcional

- **Operaciones base:** `multiply` (suma repetida) y `divide` (resta repetida).
- **Composición:** el resultado de una operación alimenta a la siguiente, por ejemplo `((5 * 4) / 10) * 6 = 12`.
- **Callbacks:** `multiplyCall` y `divideCall` reciben una función de éxito y una de error, y validan parámetros faltantes y división entre cero.
- **Promesas:** `multiplyPromise` y `dividePromise` se encadenan con `.then()` y los errores se atrapan con `.catch()`.
- **Async/await:** la función `operations` resuelve la misma cadena de operaciones de forma secuencial.

Salida esperada (resumen):

```text
20, 4, 2, 12                  <- funciones y composición
=========== CallBacks ==========
20, 80, 5, 2, 12, 2, 12       <- resultados de los callbacks
========== Promises ==========
============ ASYNC / AWAIT ============
{ n1: 20 } { n1: 5 } ...      <- resultados de las promesas y de async/await
```

Los resultados de promesas y `async/await` se imprimen después de las líneas de encabezado porque son asíncronos: JavaScript termina primero el código síncrono y después atiende las promesas.

### `poo.js`: orientación a objetos

- **Clase base:** `Animal` guarda el nombre y una función que define su sonido; incluye `sound()`, `comer()`, getter y setter de `name` y el método estático `isAnimal(obj)`.
- **Herencia:** `Dog` y `Cat` extienden de `Animal` con `extends` y `super`, y agregan la propiedad `type` con su getter y setter.
- **`instanceof`:** `Animal.isAnimal(...)` devuelve `true` para un `Animal` y `false` para un `Robot`.
- **Polimorfismo:** cada animal de la lista responde a `sound()` con su propio sonido.

Salida esperada:

```text
perro
{ _name: 'perro' }
gato
estoy comiendo
 El objeto es un animal? true
 El objeto es un animal? false
 El objeto es un animal? true
guau guau!
Miau Miau!
```

## Estructura general del proyecto

```text
javascript-fundamentals/
|-- app.js
|-- cal.js
|-- poo.js
`-- README.md
```

## Autora

Giovanna Paulina Hernández Mendoza — 377284
