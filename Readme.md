# Curso de Programación en C #

## Índice

- [Curso de Programación en C](#curso-de-programación-en-c)
  - [Índice](#índice)
  - [1.- Uso de la Línea de Comandos (CMD)](#1--uso-de-la-línea-de-comandos-cmd)
    - [1.1.- ¿Para qué sirve?](#11--para-qué-sirve)
    - [1.2.- Comandos Básicos](#12--comandos-básicos)
  - [2.- Ambiente de Trabajo en C](#2--ambiente-de-trabajo-en-c)
    - [2.1 Instalación del SDK de .NET](#21-instalación-del-sdk-de-net)
      - [2.1.1 Historia de los compiladores](#211-historia-de-los-compiladores)
      - [2.1.2 Instrucciones de Descarga](#212-instrucciones-de-descarga)
    - [2.2 Descarga de IDE](#22-descarga-de-ide)
      - [Opción 1: Visual Studio Code (Ligero y rápido)](#opción-1-visual-studio-code-ligero-y-rápido)
      - [Opción 2: Visual Studio Community (Completo y profesional)](#opción-2-visual-studio-community-completo-y-profesional)
  - [3.- Primeros Pasos en C](#3--primeros-pasos-en-c)
    - [3.1 Tu primer "Hola, Mundo"](#31-tu-primer-hola-mundo)
      - [Versión Antigua (C# 1.0 - 7.0)](#versión-antigua-c-10---70)
      - [Versión Moderna (C# 9 y superior)](#versión-moderna-c-9-y-superior)
    - [3.2 Compilación y Ejecución](#32-compilación-y-ejecución)
      - [3.2.1 🧠 ¿Qué es compilar?](#321--qué-es-compilar)
      - [3.2.2⚙️ Compilación desde la Línea de Comandos](#322️-compilación-desde-la-línea-de-comandos)
        - [3.2.2.1 Paso 1: Crear el archivo](#3221-paso-1-crear-el-archivo)
        - [3.2.2.2 Paso 2: Compilar con el SDK de .NET](#3222-paso-2-compilar-con-el-sdk-de-net)
        - [3.2.2.3 Paso 3: Ejecutar el programa](#3223-paso-3-ejecutar-el-programa)
      - [3.2.3 💻 Compilación y Ejecución en Visual Studio Code](#323--compilación-y-ejecución-en-visual-studio-code)
      - [🧩 3.2.4 ¿Qué sucede durante la ejecución?](#-324-qué-sucede-durante-la-ejecución)
      - [⚡ 3.2.5 Errores Comunes al Compilar](#-325-errores-comunes-al-compilar)
      - [🧮 3.2.6 Extra: Compilación de varios archivos](#-326-extra-compilación-de-varios-archivos)
      - [🎯 3.2.7 Resumen](#-327-resumen)
  - [4.- Bits y Bytes de Información](#4--bits-y-bytes-de-información)
    - [4.1 ¿Qué es un Bit?](#41-qué-es-un-bit)
    - [4.2 ¿Qué es un Byte?](#42-qué-es-un-byte)
    - [4.3 Conversión entre Bits y Bytes](#43-conversión-entre-bits-y-bytes)
    - [4.4 Ejemplo de Conversión](#44-ejemplo-de-conversión)
      - [Ejemplo 1: Bits a Bytes](#ejemplo-1-bits-a-bytes)
      - [Ejemplo 2: Bytes a Bits](#ejemplo-2-bytes-a-bits)
      - [Ejemplo 3: Representando un texto](#ejemplo-3-representando-un-texto)
      - [Ejemplo 4: Tamaños comunes en informática](#ejemplo-4-tamaños-comunes-en-informática)
    - [4.5 Importancia en Programación](#45-importancia-en-programación)
  - [5.- Tipos de Datos en C# – Variables y Constantes](#5--tipos-de-datos-en-c--variables-y-constantes)
    - [5.1 ¿Qué es una Variable?](#51-qué-es-una-variable)
    - [5.2 Reglas para Nombrar Variables](#52-reglas-para-nombrar-variables)
    - [5.3 Tipos de Datos Primitivos en C](#53-tipos-de-datos-primitivos-en-c)
      - [🧮 Tipos Numéricos Enteros](#-tipos-numéricos-enteros)
      - [🔢 Tipos Numéricos de Punto Flotante](#-tipos-numéricos-de-punto-flotante)
      - [🔠 Tipos de Texto y Caracteres](#-tipos-de-texto-y-caracteres)
      - [💡 Tipo Lógico (Booleano)](#-tipo-lógico-booleano)
    - [5.4 Variables vs. Constantes](#54-variables-vs-constantes)
    - [5.5 Inferencia de Tipos (`var` y `dynamic`)](#55-inferencia-de-tipos-var-y-dynamic)
      - [🔹 `var` (Tipo Inferido en tiempo de compilación)](#-var-tipo-inferido-en-tiempo-de-compilación)
      - [🔹 `dynamic` (Tipo dinámico en tiempo de ejecución)](#-dynamic-tipo-dinámico-en-tiempo-de-ejecución)
    - [5.6 Ejemplo General en C](#56-ejemplo-general-en-c)
    - [5.7 Recomendaciones Profesionales](#57-recomendaciones-profesionales)
  - [6.- Más sobre Strings](#6--más-sobre-strings)
    - [6.1 Introducción a los Strings en C](#61-introducción-a-los-strings-en-c)
    - [6.2 Manipulación de Strings (Concatenación, Subcadenas, Búsqueda)](#62-manipulación-de-strings-concatenación-subcadenas-búsqueda)
      - [🔹 6.2.1 Concatenación: unir varios strings](#-621-concatenación-unir-varios-strings)
        - [🔹 Concatenación con el operador `+`](#-concatenación-con-el-operador-)
        - [🔹 Concatenación con `string.Concat()`](#-concatenación-con-stringconcat)
        - [🔹 Concatenación con interpolación (`$""`)](#-concatenación-con-interpolación-)
        - [💡 **Resumen de las tres formas:**](#-resumen-de-las-tres-formas)
      - [🔹 6.2.2 Subcadenas: extraer una parte del texto](#-622-subcadenas-extraer-una-parte-del-texto)
      - [🔹 6.2.3 Búsqueda: localizar texto dentro de un string](#-623-búsqueda-localizar-texto-dentro-de-un-string)
    - [6.3 Formateo de Strings](#63-formateo-de-strings)
    - [6.4 Interpolación de Strings](#64-interpolación-de-strings)
    - [6.5 Métodos Comunes de la Clase String](#65-métodos-comunes-de-la-clase-string)
    - [6.6 Uso de StringBuilder para Cadenas Grandes](#66-uso-de-stringbuilder-para-cadenas-grandes)
    - [6.7 Codificación y Unicode](#67-codificación-y-unicode)
    - [6.8 Expresiones Regulares](#68-expresiones-regulares)
    - [6.9 Internacionalización y Localización de Strings](#69-internacionalización-y-localización-de-strings)
    - [6.10 Optimización del Rendimiento con Strings](#610-optimización-del-rendimiento-con-strings)
    - [6.11 Buenas Prácticas en el Manejo de Strings](#611-buenas-prácticas-en-el-manejo-de-strings)
    - [6.12 Ejemplos Prácticos y Ejercicios](#612-ejemplos-prácticos-y-ejercicios)

---

## 1.- Uso de la Línea de Comandos (CMD)

La **Línea de Comandos** (también conocida como **CMD** o Símbolo del Sistema) es una potente herramienta que te permite interactuar con tu sistema operativo mediante comandos de texto.
En lugar de hacer clic en iconos y menús, escribes comandos para realizar tareas.
Se encuentra en todos los Sistemas Operativos bajo diferentes nombres y comandos.

| Sistema Operativo | Basado en | Nombre del intérprete |
| :---------------- | :-------- | :-------------------- |
| Windows           | DOS       | CMD o PowerShell      |
| Linux             | UNIX      | Bash                  |
| macOS             | UNIX      | Terminal              |

### 1.1.- ¿Para qué sirve?

Sirve para ejecutar programas, administrar archivos y carpetas, automatizar tareas y solucionar problemas del sistema.
Es una habilidad fundamental para cualquier programador, ya que te da un control más directo y eficiente sobre el computador.

### 1.2.- Comandos Básicos

Aquí tienes algunos de los comandos más esenciales al menos en Windows para empezar:

| Comando           | Descripción                                            | Ejemplo                |
| :---------------- | :----------------------------------------------------- | :--------------------- |
| `dir`             | Lista los archivos y carpetas en el directorio actual. | `dir`                  |
| `cd <directorio>` | Cambia el directorio actual.                           | `cd Documentos`        |
| `mkdir <nombre>`  | Crea una nueva carpeta.                                | `mkdir ProyectoCSharp` |
| `echo <texto>`    | Muestra un mensaje en la consola.                      | `echo Hola Mundo`      |
| `cls`             | Limpia la pantalla.                                    | `cls`                  |

---

## 2.- Ambiente de Trabajo en C #

### 2.1 Instalación del SDK de .NET

Para poder programar en C#, necesitas el **SDK de .NET** (Software Development Kit).
Este paquete incluye todo lo necesario para crear y ejecutar aplicaciones en C#:

- **Compilador de C# (Roslyn):** Traduce tu código a lenguaje intermedio (IL).
- **Runtime de .NET:** Ejecuta el código compilado.
- **Bibliotecas Base:** Conjunto de clases listas para usar (manejo de archivos, fechas, cadenas, etc.).

#### 2.1.1 Historia de los compiladores

| Fecha | Evento / Hito           | Breve Descripción                                                                       |
| :---- | :---------------------- | :-------------------------------------------------------------------------------------- |
| 1952  | A-0 System              | Creado por Grace Hopper, el primer compilador. Traducía código a subrutinas.            |
| 1957  | FORTRAN                 | Primer compilador completo, desarrollado por John Backus en IBM.                        |
| 1972  | Lenguaje C              | El compilador de C, creado por Dennis Ritchie, revolucionó la programación.             |
| 2002  | C# 1.0 y .NET Framework | Microsoft lanza C# junto con su compilador para el CLR (Common Language Runtime).       |
| 2014  | Roslyn                  | El compilador de C# fue reescrito en C# y liberado como open source.                    |
| 2020  | .NET 5                  | Unificación de .NET Framework, .NET Core y Mono en una sola plataforma multiplataforma. |

#### 2.1.2 Instrucciones de Descarga

1. Entra a la página oficial: [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
2. Descarga el SDK de .NET más reciente para tu sistema operativo.
3. Instálalo siguiendo las instrucciones.
4. Verifica la instalación ejecutando en la terminal:

   ```bash
   dotnet --version
   ```

   Si aparece un número de versión (por ejemplo, `8.0.301`), la instalación fue exitosa.

---

### 2.2 Descarga de IDE

Un **IDE** (Entorno de Desarrollo Integrado) facilita el proceso de programación con herramientas visuales, autocompletado, depuración y resaltado de sintaxis.

#### Opción 1: Visual Studio Code (Ligero y rápido)

1. Descarga desde: [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Instálalo (marca la opción **"Add to PATH"**).
3. Instala la extensión **C# Dev Kit** de Microsoft.
4. Crea un nuevo proyecto:

   ```bash
   dotnet new console -n MiPrimerProyecto
   cd MiPrimerProyecto
   code .
   ```

#### Opción 2: Visual Studio Community (Completo y profesional)

1. Descarga desde: [https://visualstudio.microsoft.com/](https://visualstudio.microsoft.com/)
2. Durante la instalación, marca las cargas de trabajo:

   - **.NET desktop development**
   - **ASP.NET and web development**
3. Ideal para proyectos grandes o de tipo empresarial.

---

## 3.- Primeros Pasos en C #

### 3.1 Tu primer "Hola, Mundo"

El clásico primer programa para aprender un lenguaje.

#### Versión Antigua (C# 1.0 - 7.0)

Antes de C# 9, era obligatorio escribir toda la estructura del programa con su clase principal y método `Main`.

```csharp
// Ejemplo clásico de "Hola Mundo" en versiones antiguas de C#
using System;

namespace MiPrimerPrograma
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hola, Mundo!");
        }
    }
}
```

**¿Qué significa cada parte?**

- `using System;`
  Indica que se usará el espacio de nombres **System**, donde está la clase `Console`.

- `namespace MiPrimerPrograma`
  Agrupa el código bajo un “espacio de nombres”.
  Sirve para organizar el código y evitar conflictos entre clases con el mismo nombre.

- `class Program`
  Define una clase llamada **Program** (toda aplicación en C# se organiza en clases).

- `static void Main(string[] args)`
  Es el **punto de entrada** del programa.
  El método `Main` se ejecuta automáticamente al iniciar el programa.

  - `static`: significa que se puede ejecutar sin crear una instancia de la clase.
  - `void`: indica que no devuelve ningún valor.
  - `string[] args`: permite recibir argumentos desde la línea de comandos.

- `Console.WriteLine("Hola, Mundo!");`
  Imprime el mensaje `"Hola, Mundo!"` en la consola y salta a la siguiente línea.

#### Versión Moderna (C# 9 y superior)

En las versiones modernas de C#, escribir un programa es tan simple como:

```csharp
// Esto es un programa completo en C# moderno.
Console.WriteLine("Hola, Mundo!");
```

**¿Qué significa cada parte?**

- `Console` → Es una clase del espacio de nombres `System` que permite interactuar con la consola.
  (Leer, escribir texto, limpiar pantalla, etc.)

- `WriteLine("Hola, Mundo!")` → Es un **método** de la clase `Console` que imprime el texto dentro de los paréntesis y luego agrega un salto de línea.

> 💡 En C# moderno, ya no es necesario declarar una clase o un método `Main` explícitamente para programas simples.
> El compilador lo hace por ti, ideal para ejemplos o scripts rápidos.

---

> **Importante**
> Aunque esta simplificación es conveniente, es recomendable entender la estructura completa de un programa en C# para proyectos más grandes y complejos.
> La clase debe de llamarse igual que el archivo donde se guarda el código.
> Por ejemplo, si el archivo se llama `Programa.cs`, la clase debe llamarse `Programa`.
> Esto ayuda a mantener el código organizado y fácil de entender.
> Además, en proyectos más grandes, es necesario definir explícitamente la estructura del programa.

---

### 3.2 Compilación y Ejecución

Una vez que has escrito tu primer programa en C#, el siguiente paso es **compilarlo** y **ejecutarlo**.
Esto significa transformar tu código fuente (`.cs`) en un programa que el sistema pueda entender y ejecutar.

---

#### 3.2.1 🧠 ¿Qué es compilar?

**Compilar** es el proceso de traducir el código que tú escribes (en C#) a un lenguaje intermedio llamado **IL (Intermediate Language)**.
Este código intermedio luego es interpretado por el **CLR (Common Language Runtime)** del .NET, que finalmente lo ejecuta.

> En resumen:
>
> - Tú escribes código C# → el compilador genera IL → el CLR lo ejecuta.

---

#### 3.2.2⚙️ Compilación desde la Línea de Comandos

Si no estás usando un IDE (solo el **CMD** o la **terminal**), puedes compilar manualmente tu programa.

##### 3.2.2.1 Paso 1: Crear el archivo

Crea un archivo llamado `HolaMundo.cs` con el siguiente contenido:

```csharp
using System;

class HolaMundo
{
    static void Main()
    {
        Console.WriteLine("Hola, Mundo!");
    }
}
```

Guárdalo en una carpeta fácil de acceder, por ejemplo:
`C:\ProyectosCSharp\HolaMundo`

---

##### 3.2.2.2 Paso 2: Compilar con el SDK de .NET

Abre la **línea de comandos** en esa carpeta y ejecuta:

```bash
dotnet new console -n HolaMundo
cd HolaMundo
```

Esto creará automáticamente un proyecto con la estructura básica de C#.

> 💡 Si ya tienes un archivo `.cs` suelto, también puedes compilarlo manualmente con:
>
> ```bash
> csc HolaMundo.cs
> ```
>
> donde `csc` es el **compilador de C# (C Sharp Compiler)** incluido en el SDK.

---

##### 3.2.2.3 Paso 3: Ejecutar el programa

Una vez compilado, puedes ejecutarlo de dos formas:

1. Si usaste `dotnet new`, el proyecto genera una carpeta con un archivo `.dll` dentro de `bin/Debug/net8.0/`.
   Ejecuta el programa con:

   ```bash
   dotnet run
   ```

   o también:

   ```bash
   dotnet bin/Debug/net8.0/HolaMundo.dll
   ```

2. Si usaste `csc`, se generará un archivo ejecutable (`HolaMundo.exe` en Windows).
   Ejecútalo directamente con:

   ```bash
   HolaMundo
   ```

> ✅ Si ves el mensaje `Hola, Mundo!`, ¡felicidades! has compilado y ejecutado tu primer programa en C# correctamente.

---

#### 3.2.3 💻 Compilación y Ejecución en Visual Studio Code

Si prefieres usar **Visual Studio Code**, sigue estos pasos:

1. Abre la carpeta del proyecto (`HolaMundo`).
2. Asegúrate de tener instaladas las extensiones:

   - **C# Dev Kit**
   - **.NET Install Tool**
3. Abre el archivo `Program.cs`.
4. Presiona **F5** o haz clic en **Ejecutar > Iniciar depuración**.

Visual Studio Code automáticamente compila y ejecuta tu código usando el SDK de .NET.

> 💡 El resultado aparecerá en el panel de “Terminal Integrada” al final del editor.

---

#### 🧩 3.2.4 ¿Qué sucede durante la ejecución?

Cuando ejecutas el comando `dotnet run`, el proceso sigue estos pasos:

1. El SDK de .NET **compila** tu código fuente en un lenguaje intermedio (**IL**).
2. Ese IL se guarda en un archivo **.dll**.
3. El **CLR (Common Language Runtime)** traduce dinámicamente el IL a **código máquina nativo**.
4. Tu procesador ejecuta ese código y muestra la salida por consola.

> En pocas palabras, tu código pasa por un proceso de **traducción en tiempo real**, lo que permite a C# ser **multiplataforma** (Windows, Linux, macOS).

---

#### ⚡ 3.2.5 Errores Comunes al Compilar

| Error                                                     | Causa Común                                | Solución                                            |
| :-------------------------------------------------------- | :----------------------------------------- | :-------------------------------------------------- |
| `error CS1002: ; expected`                                | Olvidaste un punto y coma `;`              | Revisa las líneas del código.                       |
| `The type or namespace name 'Console' could not be found` | Falta el `using System;`                   | Agrégalo al inicio del archivo.                     |
| `dotnet: command not found`                               | No está instalado o no está en el PATH     | Reinstala el SDK y marca la opción **Add to PATH**. |
| `Program does not contain a static Main method`           | Falta el método `Main` o está mal definido | Corrige la firma del método principal.              |

---

#### 🧮 3.2.6 Extra: Compilación de varios archivos

Si tu proyecto tiene varios archivos `.cs`, puedes compilarlos todos al mismo tiempo:

```bash
csc *.cs
```

Esto generará un único ejecutable `programa.exe` que incluye todas las clases.

---

#### 🎯 3.2.7 Resumen

| Acción               | Comando / Paso                       |
| :------------------- | :----------------------------------- |
| Crear nuevo proyecto | `dotnet new console -n MiApp`        |
| Entrar a la carpeta  | `cd MiApp`                           |
| Compilar y ejecutar  | `dotnet run`                         |
| Compilar manualmente | `csc Archivo.cs`                     |
| Ejecutar ejecutable  | `Archivo.exe` o `dotnet Archivo.dll` |

---

> 🧠 **Tip del Pro:**
> Si usas Visual Studio (no Code), al presionar **Ctrl + F5** el IDE compila y ejecuta tu programa automáticamente, mostrando la consola sin cerrarla al terminar.
> Esto es ideal para ver los resultados sin tener que abrir la terminal aparte.

---
Perfecto ⚙️ Aquí tienes tu sección **4.- Bits y Bytes de Información** completamente ampliada, manteniendo el mismo formato, tono y orden de títulos, pero con explicaciones más profundas, ejemplos claros y comparaciones prácticas para entenderlo a la perfección 👇

---

## 4.- Bits y Bytes de Información

### 4.1 ¿Qué es un Bit?

- Un **bit** (abreviatura de *binary digit*, “dígito binario”) es la **unidad mínima de información** que puede manejar una computadora.
- Solo puede tener **dos valores posibles**:

  - `0` → apagado, falso o sin energía.
  - `1` → encendido, verdadero o con energía.

🧠 **Ejemplo práctico:**
Imagina un interruptor de luz:

- Apagado = `0`
- Encendido = `1`
  Un bit es ese interruptor, pero a nivel electrónico.

💡 En el hardware, los bits se representan mediante **voltajes eléctricos** (por ejemplo, 0V = 0 y 5V = 1), **polaridad magnética** o **niveles ópticos** dependiendo del dispositivo.

---

### 4.2 ¿Qué es un Byte?

- Un **byte** está formado por **8 bits consecutivos**, agrupados para representar información más compleja.
- Un byte puede representar **256 combinaciones distintas** (2⁸ = 256), es decir, valores del **0 al 255** en decimal.

🧩 **Ejemplo:**

| Bits     | Valor decimal | Valor binario                |
| :------- | :------------ | :--------------------------- |
| 00000000 | 0             | Todo apagado                 |
| 00000001 | 1             | Solo el último bit encendido |
| 11111111 | 255           | Todos los bits encendidos    |

📘 **Dato curioso:**
Un byte suele representar **un solo carácter** de texto.
Por ejemplo:

- `'A'` → 65
- `'B'` → 66
- `'a'` → 97
- `' '` (espacio) → 32

Esto se basa en la **tabla ASCII**, un estándar que asigna un número a cada carácter.

---

### 4.3 Conversión entre Bits y Bytes

Para trabajar correctamente con información binaria, es fundamental saber convertir entre bits y bytes.

- **De bits a bytes:** divide entre 8
  🧮 Fórmula → `Bytes = Bits / 8`

- **De bytes a bits:** multiplica por 8
  🧮 Fórmula → `Bits = Bytes × 8`

📘 **Ejemplos de conversión:**

| Cantidad  | Conversión | Resultado |
| :-------- | :--------- | :-------- |
| 8 bits    | ÷ 8        | 1 byte    |
| 16 bits   | ÷ 8        | 2 bytes   |
| 32 bits   | ÷ 8        | 4 bytes   |
| 4 bytes   | × 8        | 32 bits   |
| 128 bytes | × 8        | 1024 bits |

> ⚡ **Regla fácil de recordar:**
>
> - Multiplica por 8 para pasar de **bytes a bits**.
> - Divide entre 8 para pasar de **bits a bytes**.

---

### 4.4 Ejemplo de Conversión

Vamos con algunos ejemplos más ilustrativos 🔍

#### Ejemplo 1: Bits a Bytes

Supón que tienes **64 bits** de información.

- Aplicamos la fórmula: `64 / 8 = 8`
  ➡️ **Resultado:** 64 bits equivalen a **8 bytes**.

#### Ejemplo 2: Bytes a Bits

Tienes un archivo de **10 bytes**.

- Aplicamos la fórmula: `10 × 8 = 80`
  ➡️ **Resultado:** 10 bytes equivalen a **80 bits**.

#### Ejemplo 3: Representando un texto

Si escribes la palabra `"Hola"` en un archivo de texto plano:

- Cada letra ocupa **1 byte** (en codificación ASCII).
- `"Hola"` tiene 4 caracteres → **4 bytes = 32 bits.**

Al final Hola en bits sería:
'01001000 01101111 01101100 01100001'

- `H` = 01001000
- `o` = 01101111
- `l` = 01101100
- `a` = 01100001

#### Ejemplo 4: Tamaños comunes en informática

| Unidad          | Equivalencia | Aproximado         |
| :-------------- | :----------- | :----------------- |
| 1 Byte          | 8 bits       | Un carácter        |
| 1 Kilobyte (KB) | 1024 bytes   | Un párrafo corto   |
| 1 Megabyte (MB) | 1024 KB      | Una imagen pequeña |
| 1 Gigabyte (GB) | 1024 MB      | Un video corto     |
| 1 Terabyte (TB) | 1024 GB      | Miles de películas |

> 📦 Así puedes imaginar la escala:
> **bit < byte < kilobyte < megabyte < gigabyte < terabyte**

---

### 4.5 Importancia en Programación

Comprender los **bits** y **bytes** es fundamental en el mundo de la programación porque todo lo que hace una computadora se basa en ellos.

💡 **Aplicaciones clave:**

1. **Optimización de Memoria:**

   - Saber cuánto ocupa cada tipo de dato evita desperdiciar memoria.
     Ejemplo:

     | Tipo de Dato | Tamaño en Bytes | Rango aproximado               |
     | :----------- | :-------------- | :----------------------------- |
     | `bool`       | 1 byte          | true / false                   |
     | `char`       | 1 byte          | 0 a 255                        |
     | `int`        | 4 bytes         | -2,147,483,648 a 2,147,483,647 |
     | `float`      | 4 bytes         | Números decimales simples      |
     | `double`     | 8 bytes         | Mayor precisión decimal        |

2. **Manipulación de Datos Binarios:**

   - En programación de bajo nivel (como sistemas embebidos o videojuegos), se trabajan directamente los bits mediante **operadores bit a bit** (`&`, `|`, `^`, `<<`, `>>`).

   🔧 Ejemplo:

   ```csharp
   int valor = 5;      // En binario: 0101
   int resultado = valor << 1;  // Desplaza los bits a la izquierda → 1010 (decimal 10)
   Console.WriteLine(resultado); // Imprime 10
   ```

3. **Comunicaciones y Redes:**

   - Las velocidades de internet se miden en **bits por segundo (bps)**, no en bytes.

     - Ejemplo:
       100 Mbps = 100 millones de bits por segundo ≈ 12.5 MB/s reales.

4. **Criptografía y Seguridad:**

   - Los algoritmos de cifrado (como AES-256) usan claves de cierto número de **bits**.
     Cuantos más bits, mayor seguridad.

---

> 🧠 **Resumen Final:**
>
> - **Bit:** unidad mínima (0 o 1).
> - **Byte:** 8 bits.
> - **Conversión:** bits ↔ bytes (×8 o ÷8).
> - **Importancia:** todo en programación, memoria, red y seguridad depende de ellos.

---

## 5.- Tipos de Datos en C# – Variables y Constantes

En C#, todos los datos que usas en tus programas se almacenan temporalmente en memoria mediante **variables** o **constantes**.
Comprender los **tipos de datos** y su tamaño en **bits** y **bytes** es esencial para escribir código eficiente y sin errores.

---

### 5.1 ¿Qué es una Variable?

Una **variable** es un espacio reservado en memoria que puede **cambiar su valor durante la ejecución** del programa.
Se le da un **nombre**, un **tipo de dato** y un **valor**.

📘 **Sintaxis general:**

```csharp
tipo nombre = valor;
```

🧩 **Ejemplo:**

```csharp
int edad = 28;
string nombre = "LechuDev";
double altura = 1.78;
```

📦 **Explicación:**

- `int` → Tipo de dato (número entero).
- `edad` → Nombre de la variable.
- `28` → Valor almacenado.

💡 Las variables permiten **almacenar, modificar y utilizar información** en distintas partes del programa.

---

### 5.2 Reglas para Nombrar Variables

C# tiene reglas específicas para asignar nombres válidos a las variables:

✅ **Permitido:**

- Comienzan con una letra o guion bajo `_`
- Pueden contener números (pero no al inicio)
- Distinguen entre mayúsculas y minúsculas

🚫 **No permitido:**

- Empezar con un número (`2edad ❌`)
- Usar espacios o símbolos especiales (`mi edad ❌`)
- Usar palabras reservadas del lenguaje (`int`, `class`, `for`, etc.)

🧠 **Ejemplos válidos:**

```csharp
string nombreUsuario;
int _contador;
float velocidadMaxima;
```

---

### 5.3 Tipos de Datos Primitivos en C #

C# ofrece varios **tipos de datos primitivos**, cada uno diseñado para almacenar una clase específica de información.

#### 🧮 Tipos Numéricos Enteros

| Tipo    | Tamaño            | Rango aproximado | Ejemplo                        |
| :------ | :---------------- | :--------------- | :----------------------------- |
| `byte`  | 8 bits (1 byte)   | 0 a 255          | `byte edad = 25;`              |
| `sbyte` | 8 bits            | -128 a 127       | `sbyte temperatura = -10;`     |
| `short` | 16 bits (2 bytes) | -32,768 a 32,767 | `short año = 2025;`            |
| `int`   | 32 bits (4 bytes) | ±2,147,483,647   | `int puntos = 5000;`           |
| `long`  | 64 bits (8 bytes) | ±9.22×10¹⁸       | `long estrellas = 9876543210;` |

> 🧠 *Consejo:* Usa `int` por defecto, a menos que necesites números extremadamente grandes o quieras optimizar memoria en estructuras grandes.

---

#### 🔢 Tipos Numéricos de Punto Flotante

| Tipo      | Tamaño              | Precisión                      | Ejemplo                         |
| :-------- | :------------------ | :----------------------------- | :------------------------------ |
| `float`   | 32 bits (4 bytes)   | 6–7 decimales                  | `float temperatura = 36.5f;`    |
| `double`  | 64 bits (8 bytes)   | 15–16 decimales                | `double pi = 3.14159265358979;` |
| `decimal` | 128 bits (16 bytes) | Alta precisión (28–29 dígitos) | `decimal dinero = 99.99m;`      |

> 💡 *Diferencia:*
>
> - `float` y `double` se usan para cálculos científicos.
> - `decimal` se usa en finanzas (porque evita errores de redondeo).

---

#### 🔠 Tipos de Texto y Caracteres

| Tipo     | Tamaño                         | Descripción              | Ejemplo                          |
| :------- | :----------------------------- | :----------------------- | :------------------------------- |
| `char`   | 16 bits (2 bytes)              | Un solo carácter Unicode | `char letra = 'A';`              |
| `string` | Variable (depende de longitud) | Cadena de texto          | `string saludo = "Hola, Mundo";` |

> 📘 En C#, los **caracteres usan comillas simples ('')**, y las **cadenas comillas dobles ("")**.

---

#### 💡 Tipo Lógico (Booleano)

| Tipo   | Tamaño | Valores posibles | Ejemplo                  |
| :----- | :----- | :--------------- | :----------------------- |
| `bool` | 1 byte | `true` o `false` | `bool encendido = true;` |

Ejemplo:

```csharp
bool esMayorDeEdad = true;
if (esMayorDeEdad)
{
    Console.WriteLine("Puedes ingresar al sistema.");
}
```

---

### 5.4 Variables vs. Constantes

| Concepto        | Variable                                   | Constante                   |
| :-------------- | :----------------------------------------- | :-------------------------- |
| **Valor**       | Puede cambiar                              | No cambia                   |
| **Declaración** | `int edad = 20;`                           | `const int AÑO = 2025;`     |
| **Uso típico**  | Datos que varían (puntaje, contador, etc.) | Datos fijos (PI, IVA, etc.) |
| **Memoria**     | Puede reasignarse                          | Permanece fija              |

🧩 **Ejemplo práctico:**

```csharp
int vidas = 3;
vidas = 2; // ✅ se puede modificar

const float PI = 3.1416f;
// PI = 3.15; ❌ error: no se puede cambiar una constante
```

> ⚠️ **Regla de oro:**
> Usa `const` para valores que nunca cambian en el programa.
> Mejora la legibilidad y evita errores.

---

### 5.5 Inferencia de Tipos (`var` y `dynamic`)

C# permite declarar variables sin especificar su tipo explícitamente.
El compilador lo **deduce automáticamente** según el valor asignado.

#### 🔹 `var` (Tipo Inferido en tiempo de compilación)

```csharp
var nombre = "LechuDev";   // Se infiere string
var edad = 28;             // Se infiere int
```

> 💡 Una vez asignado, no puedes cambiar su tipo:
>
> ```csharp
> var x = 10;
> x = "Hola"; // ❌ Error, no puedes cambiar de int a string
> ```

#### 🔹 `dynamic` (Tipo dinámico en tiempo de ejecución)

```csharp
dynamic dato = 10;
dato = "ahora soy texto"; // ✅ permitido
```

> ⚠️ Menos seguro, pero útil cuando el tipo no se conoce hasta la ejecución (por ejemplo, datos de JSON o bases de datos).

---

### 5.6 Ejemplo General en C #

```csharp
using System;

class TiposDeDatos
{
    static void Main()
    {
        // Enteros
        int edad = 28;
        long población = 8000000;

        // Decimales
        float temperatura = 36.5f;
        double pi = 3.1415926535;

        // Texto
        char inicial = 'L';
        string nombre = "LechuDev";

        // Booleano
        bool activo = true;

        // Constante
        const int ANO = 2025;

        // Mostrar resultados
        Console.WriteLine($"Hola, soy {nombre} ({inicial})");
        Console.WriteLine($"Edad: {edad} años");
        Console.WriteLine($"Temperatura corporal: {temperatura}°C");
        Console.WriteLine($"Valor de PI: {pi}");
        Console.WriteLine($"¿Activo? {activo}");
        Console.WriteLine($"Año actual: {ANO}");
    }
}
```

🧠 **Salida esperada:**

```yaml
Hola, soy LechuDev (L)
Edad: 28 años
Temperatura corporal: 36.5°C
Valor de PI: 3.1415926535
¿Activo? True
Año actual: 2025
```

---

### 5.7 Recomendaciones Profesionales

✅ Usa **nombres descriptivos**:
Evita variables como `x`, `y` o `dato1`. Prefiere `contadorUsuarios`, `temperaturaCelsius`, etc.

✅ Declara **constantes** para valores fijos (como `const float IVA = 0.16f;`).

✅ Elige el **tipo más pequeño posible** para optimizar memoria, especialmente en estructuras grandes o juegos.

✅ Usa **camelCase** para variables (`miNombre`) y **MAYÚSCULAS** para constantes (`TAMANO_BUFFER`).

✅ Aprovecha `var` solo cuando el tipo es **obvio** o mejora la legibilidad.

---

## 6.- Más sobre Strings

### 6.1 Introducción a los Strings en C #

- En C#, un **string** es una secuencia de caracteres encerrada entre comillas dobles (`" "`).
- Es un tipo de dato **inmutable**, lo que significa que una vez creado, no puede modificarse directamente.
- Ejemplo:

  ```csharp
  string saludo = "Hola, mundo";
  ```

---

### 6.2 Manipulación de Strings (Concatenación, Subcadenas, Búsqueda)

Los **strings** (cadenas de texto) en C# se pueden manipular de muchas formas.
Aquí aprenderás tres de las operaciones más comunes: **concatenar**, **extraer Subcadenas** y **buscar texto** dentro de otra cadena.

---

#### 🔹 6.2.1 Concatenación: unir varios strings

La **concatenación** consiste en unir dos o más cadenas para formar una sola.
En C#, puedes hacerlo con el operador **`+`**, el método **`Concat()`**, o la interpolación de strings (`$""`).

##### 🔹 Concatenación con el operador `+`

```csharp
string nombre = "Lechu";
string mensaje = "Hola " + nombre + "!";
Console.WriteLine(mensaje);
```

**Explicación paso a paso:**

1. `string nombre = "Lechu";`
   → Se declara una variable de tipo `string` llamada `nombre` que almacena el texto `"Lechu"`.

2. `string mensaje = "Hola " + nombre + "!";`
   → Se concatenan tres partes:

   - `"Hola "` → texto literal.
   - `nombre` → valor de la variable (`"Lechu"`).
   - `"!"` → signo de exclamación.
     El resultado es: **"Hola Lechu!"**

3. `Console.WriteLine(mensaje);`
   → Muestra el mensaje completo en consola.

**Salida:**

```nginx
Hola Lechu!
```

##### 🔹 Concatenación con `string.Concat()`

```csharp
string nombre = "Lechu";
string mensaje = string.Concat("Hola ", nombre, "!");
Console.WriteLine(mensaje);
```

**Explicación paso a paso:**

1. `string nombre = "Lechu";`
   → Se declara la variable `nombre` con el texto `"Lechu"`.

2. `string.Concat("Hola ", nombre, "!");`
   → `Concat()` une **varios strings** pasados como parámetros en **orden**.
   Resultado: `"Hola Lechu!"`.

3. `Console.WriteLine(mensaje);`
   → Imprime el mensaje concatenado en la consola.

**Salida:**

```nginx
Hola Lechu!
```

---

##### 🔹 Concatenación con interpolación (`$""`)

```csharp
string nombre = "Lechu";
string mensaje = $"Hola {nombre}!";
Console.WriteLine(mensaje);
```

**Explicación paso a paso:**

1. `string nombre = "Lechu";`
   → Declaramos la variable `nombre`.

2. `$"Hola {nombre}!"`
   → Los **corchetes `{}`** permiten insertar **el valor de cualquier variable** directamente dentro de la cadena.
   → Muy legible y moderno.

3. `Console.WriteLine(mensaje);`
   → Muestra el mensaje final.

**Salida:**

```nginx
Hola Lechu!
```

---

##### 💡 **Resumen de las tres formas:**

| Método            | Ventaja                                                            | Ejemplo                               |
| :---------------- | :----------------------------------------------------------------- | :------------------------------------ |
| `+`               | Rápido y simple                                                    | `"Hola " + nombre + "!"`              |
| `string.Concat()` | Útil para concatenar varios strings en un solo método              | `string.Concat("Hola ", nombre, "!")` |
| `$""`             | Muy legible, permite insertar variables y expresiones directamente | `$"Hola {nombre}!"`                   |

💡 *Dato:* En concatenaciones dentro de bucles o cadenas largas, se recomienda usar **`StringBuilder`** para optimizar el rendimiento.

---

#### 🔹 6.2.2 Subcadenas: extraer una parte del texto

A veces necesitas obtener solo una parte de un texto, por ejemplo, las primeras letras o una palabra dentro de una frase.
Para esto se usa el método **`Substring(inicio, longitud)`**.

```csharp
string texto = "Programación en C#";
string parte = texto.Substring(0, 12); // "Programación"
Console.WriteLine(parte);
```

**Explicación paso a paso:**

1. `string texto = "Programación en C#";`
   → Creamos una cadena con el contenido `"Programación en C#"`.

2. `texto.Substring(0, 12);`
   → `Substring()` recibe **dos parámetros**:

   - `0`: posición inicial (los strings empiezan en índice **0**).
   - `12`: número de caracteres a extraer.

   Esto devuelve los primeros 12 caracteres, que son `"Programación"`.

3. `parte` ahora contiene `"Programación"`.

4. `Console.WriteLine(parte);`
   → Muestra solo la parte extraída.

**Salida:**

```cmd
Programación
```

💡 *Consejo:* Si solo pones un parámetro, por ejemplo `texto.Substring(13)`, tomará todos los caracteres **desde el índice 13 hasta el final**.

---

#### 🔹 6.2.3 Búsqueda: localizar texto dentro de un string

Puedes **buscar texto** dentro de otro usando métodos como `IndexOf()` y `Contains()`.

```csharp
string texto = "Programación en C#";

int posicion = texto.IndexOf("C#"); // Devuelve 16
bool contiene = texto.Contains("C#"); // true

Console.WriteLine("Posición: " + posicion);
Console.WriteLine("¿Contiene 'C#'? " + contiene);
```

**Explicación paso a paso:**

1. `texto.IndexOf("C#")`
   → Busca la posición donde aparece `"C#"` dentro de la cadena.
   Como `"C#"` empieza en el **carácter número 16**, devuelve **16**.
   Si no lo encuentra, devuelve **-1**.

2. `texto.Contains("C#")`
   → Devuelve un **valor booleano (`true` o `false`)** dependiendo de si el texto contiene `"C#"` o no.

3. `Console.WriteLine()` muestra ambos resultados.

**Salida:**

```nginx
Posición: 16
¿Contiene 'C#'? True
```

💡 *Truco útil:*
Puedes combinar búsquedas y Subcadenas, por ejemplo:

```csharp
string codigo = "Lenguaje: C#";
int inicio = codigo.IndexOf(":") + 2;
string lenguaje = codigo.Substring(inicio);
Console.WriteLine(lenguaje); // C#
```

Explicación paso a paso:

1. `inicio = codigo.IndexOf(":") + 2;`
   → Busca la posición de `":"` en la cadena y le suma 2 para obtener el inicio del lenguaje.

2. `string lenguaje = codigo.Substring(inicio);`
   → Extrae la subcadena desde la posición `inicio` hasta el final.

3. `Console.WriteLine(lenguaje);`
   → Muestra el lenguaje extraído.

**Salida:**

```cmd
C#
```

---

### 6.3 Formateo de Strings

- Permite insertar valores dentro de una cadena usando **placeholders**:

  ```csharp
  string nombre = "Lechu";
  int edad = 28;
  string mensaje = string.Format("Mi nombre es {0} y tengo {1} años.", nombre, edad);
  ```

  **Explicación paso a paso:**

1. `string.Format("Mi nombre es {0} y tengo {1} años.", nombre, edad);`
   → `string.Format()` toma una cadena con **placeholders** (`{0}`, `{1}`) y reemplaza cada uno con los valores proporcionados en orden.
   - `{0}` se reemplaza por `nombre` → `"Lechu"`.
   - `{1}` se reemplaza por `edad` → `28`.
   Resultado: `"Mi nombre es Lechu y tengo 28 años."`
2. `Console.WriteLine(mensaje);`
   → Muestra el mensaje formateado en consola.
**Salida:**

```nginx
Mi nombre es Lechu y tengo 28 años.
```

---

### 6.4 Interpolación de Strings

- Es una forma moderna y más legible de insertar variables dentro de texto:

  ```csharp
  string nombre = "Lechu";
  int edad = 28;
  string mensaje = $"Mi nombre es {nombre} y tengo {edad} años.";
  ```

  **Explicación paso a paso:**

1. `$"Mi nombre es {nombre} y tengo {edad} años."`
   → El símbolo `$` antes de las comillas indica que se usará **interpolación**.
   → Los valores de las variables `nombre` y `edad` se insertan directamente en los lugares indicados por `{}`.
   Resultado: `"Mi nombre es Lechu y tengo 28 años."`
2. `Console.WriteLine(mensaje);`
   → Muestra el mensaje interpolado en consola.
**Salida:**

```nginx
Mi nombre es Lechu y tengo 28 años.
```

---

### 6.5 Métodos Comunes de la Clase String

| Método              | Descripción                           | Ejemplo                                  |
| :------------------ | :------------------------------------ | :--------------------------------------- |
| `.ToUpper()`        | Convierte a mayúsculas                | `"hola".ToUpper()` → `"HOLA"`            |
| `.ToLower()`        | Convierte a minúsculas                | `"HOLA".ToLower()` → `"hola"`            |
| `.Trim()`           | Elimina espacios al inicio y al final | `"  hola  ".Trim()` → `"hola"`           |
| `.Replace("a","o")` | Reemplaza caracteres                  | `"casa".Replace("a","o")` → `"coso"`     |
| `.Split(' ')`       | Divide por espacios u otro separador  | `"uno dos".Split(' ')` → `["uno","dos"]` |
| `.Length`          | Obtiene la longitud del string         | `"hola".Length` → `4`                    |
| `.StartsWith("H")` | Verifica si inicia con un texto         | `"Hola".StartsWith("H")` → `true`        |
| `.EndsWith("o")`    | Verifica si termina con un texto       | `"Hola".EndsWith("o")` → `true`         |
| `.IndexOf("a")`   | Busca la posición de un texto          | `"casa".IndexOf("a")` → `1`              |
| `.Contains("s")`   | Verifica si contiene un texto          | `"casa".Contains("s")` → `true`          |
| `.Substring(1,3)` | Extrae una subcadena                   | `"hola".Substring(1,3)` → `"ola"`        |
| `.Insert(2,"XX")` | Inserta texto en una posición          | `"hola".Insert(2,"XX")` → `"hoXXla"`     |
| `.Remove(1,2)` | Elimina parte del texto                 | `"hola".Remove(1,2)` → `"ha"`            |
| `.PadLeft(5)`     | Rellena a la izquierda hasta longitud   | `"hi".PadLeft(5)` → `"   hi"`            |
| `.PadRight(5)`    | Rellena a la derecha hasta longitud    | `"hi".PadRight(5)` → `"hi   "`            |
| `.IsNullOrEmpty()` | Verifica si es null o vacío            | `string.IsNullOrEmpty("")` → `true`      |
| `.IsNullOrWhiteSpace()` | Verifica si es null o solo espacios | `string.IsNullOrWhiteSpace("   ")` → `true` |
| `.CompareTo()`      | Compara dos strings                     | `"abc".CompareTo("abd")` → `-1`          |

---

### 6.6 Uso de StringBuilder para Cadenas Grandes

- La clase `StringBuilder` es ideal para construir cadenas **grandes o cambiantes**, ya que evita crear múltiples objetos en memoria.

  ```csharp
  using System.Text;
  StringBuilder sb = new StringBuilder();
  sb.Append("Hola");
  sb.Append(" ");
  sb.Append("Mundo");
  string resultado = sb.ToString(); // "Hola Mundo"
  ```

- **Explicación paso a paso:**

1. `using System.Text;`
   → Importa el espacio de nombres necesario para usar `StringBuilder`.
2. `StringBuilder sb = new StringBuilder();`
   → Crea una instancia de `StringBuilder`.
3. `sb.Append("Hola");`
4. `sb.Append(" ");`
5. `sb.Append("Mundo");`
6. `string resultado = sb.ToString();`

    → Convierte el contenido acumulado en `StringBuilder` a un string normal.
**Salida:**

```nginx
Hola Mundo
```

---

### 6.7 Codificación y Unicode

- C# usa **Unicode (UTF-16)** para representar texto, permitiendo caracteres de cualquier idioma.
- Ejemplo:

  ```csharp
  char letra = 'ñ';
  int codigo = (int)letra; // 241
  ```

- Permite trabajar con emojis, símbolos y caracteres especiales sin problemas.
- Ejemplo de emoji:

  ```csharp
  string saludo = "Hola 😊";
  Console.WriteLine(saludo);
  ```

**Salida:**

```nginx
Hola 😊
```

---

### 6.8 Expresiones Regulares

- Se utilizan para **buscar patrones** dentro de cadenas.

  ```csharp
  using System.Text.RegularExpressions;
  string texto = "Mi número es 12345";
  bool coincide = Regex.IsMatch(texto, @"\d+"); // true, porque contiene dígitos
  ```

- Permiten validar formatos (emails, teléfonos), extraer datos y reemplazar patrones complejos.
- Ejemplo de validación de email:

  ```csharp
  string email = "ejemplo@dominio.com";
  bool esValido = Regex.IsMatch(email, @"^[^@\s]+@[^@\s]+\.[^@\s]+$"); // true
  ```

  - **Explicación paso a paso:**

1. `using System.Text.RegularExpressions;`
   → Importa el espacio de nombres para usar expresiones regulares.
2. `Regex.IsMatch(texto, @"\d+");`
   → Verifica si `texto` contiene uno o más dígitos (`\d+`).
3. `Regex.IsMatch(email, @"^[^@\s]+@[^@\s]+\.[^@\s]+$");`
   → Valida si `email` tiene un formato correcto de dirección de correo electrónico.
**Salida:**

```nginx
true
true
```

---

### 6.9 Internacionalización y Localización de Strings

- Permite adaptar textos según el idioma o región del usuario.
- Se logra mediante **archivos de recursos (.resx)**.
- Ejemplo: mostrar “Hola” o “Hello” según la configuración cultural (`CultureInfo`).

- ```csharp
  using System.Globalization;
  string saludo = "Hola";
  CultureInfo cultura = new CultureInfo("en-US");
  if (cultura.TwoLetterISOLanguageName == "en")
  {
      saludo = "Hello";
  }
  Console.WriteLine(saludo);
  ```

- **Explicación paso a paso:**

1. `using System.Globalization;`
   → Importa el espacio de nombres para trabajar con internacionalización.
2. `string saludo = "Hola";`
   → Texto en inglés.
3. `CultureInfo cultura = new CultureInfo("en-US");`
   → Configuración cultural en inglés.
4. `if (cultura.TwoLetterISOLanguageName == "en")`
    → Verifica si el idioma es inglés.
5. `saludo = "Hello";`
   → Cambia el saludo a inglés si es necesario.
6. `Console.WriteLine(saludo);`
   → Muestra el saludo adaptado.
**Salida:**

```nginx
Hello
```

---

### 6.10 Optimización del Rendimiento con Strings

- Usa `StringBuilder` para concatenaciones en bucles.
- Evita concatenar muchas cadenas con `+`.
- Reutiliza variables cuando sea posible.
- Prefiere interpolación (`$" "`) sobre `string.Format()` por claridad y eficiencia.
- Ejemplo de optimización:

```csharp
StringBuilder sb = new StringBuilder();
for (int i = 0; i < 1000; i++)
{
    sb.Append("Número: " + i + "\n");
}
string resultado = sb.ToString();
```

**Explicación paso a paso:**

1. `StringBuilder sb = new StringBuilder();`
   → Crea un `StringBuilder` vacío.
2. `for (int i = 0; i < 1000; i++)`
   → Itera 1000 veces.
3. `sb.Append("Número: " + i + "\n");`
   → Añade cada número al `StringBuilder`.
4. `string resultado = sb.ToString();`
   → Convierte el contenido a un string final.
**Salida:**

```nginx
Número: 0
Número: 1
Número: 2
...Número: 999
```

---

### 6.11 Buenas Prácticas en el Manejo de Strings

- Evita valores **null** (usa `string.Empty` o `""`).
- Usa métodos de comparación seguros:

  ```csharp
  if (string.Equals(a, b, StringComparison.OrdinalIgnoreCase)) { }
  ```

  Explicación paso a paso:

1. `string.Equals(a, b, StringComparison.OrdinalIgnoreCase)`
   → Compara dos cadenas `a` y `b` sin importar mayúsculas o minúsculas.

- Maneja excepciones al trabajar con strings (IndexOutOfRange, NullReference).

- Limpia la entrada de usuario (Trim, Replace, Validaciones).
- Documenta el propósito de cadenas complejas.
- Considera la **internacionalización** desde el inicio.
- Prefiere `StringBuilder` para operaciones intensivas.
 Salida esperada:

```nginx
true
```

---

### 6.12 Ejemplos Prácticos y Ejercicios

- Concatenar nombre y apellido.

```csharp
string nombre = "Lechu";
string apellido = "Dev";
string nombreCompleto = nombre + " " + apellido;
Console.WriteLine(nombreCompleto); // Salida: Lechu Dev

- Buscar si una palabra contiene “C#”.
```csharp
string texto = "Aprendiendo C# es divertido";
bool contieneCSharp = texto.Contains("C#");
Console.WriteLine(contieneCSharp); // Salida: True
```

- Extraer las 3 primeras letras de un string.

```csharp
string palabra = "Programación";
string primerasTres = palabra.Substring(0, 3);
Console.WriteLine(primerasTres); // Salida: Pro
```

- Reemplazar todos los espacios por guiones.

```csharp
string frase = "Hola mundo desde C#";
string fraseConGuiones = frase.Replace(" ", "-");
Console.WriteLine(fraseConGuiones); // Salida: Hola-mundo-desde-C#
```

- Convertir texto a mayúsculas.

```csharp
string mensaje = "hola lechudev";
string mensajeMayusculas = mensaje.ToUpper();
Console.WriteLine(mensajeMayusculas); // Salida: HOLA LECHUDEV
```

---
