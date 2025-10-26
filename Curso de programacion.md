# Curso de Programación en C#

## Índice

- [Curso de Programación en C#](#curso-de-programación-en-c)
  - [Índice](#índice)
  - [1.- Uso de la Línea de Comandos (CMD)](#1--uso-de-la-línea-de-comandos-cmd)
    - [1.1.- ¿Para qué sirve?](#11--para-qué-sirve)
    - [1.2.- Comandos Básicos](#12--comandos-básicos)
  - [2.- Ambiente de Trabajo en C#](#2--ambiente-de-trabajo-en-c)
    - [2.1 Instalación del SDK de .NET](#21-instalación-del-sdk-de-net)
      - [2.1.1 Historia de los compiladores](#211-historia-de-los-compiladores)
      - [2.1.2 Instrucciones de Descarga](#212-instrucciones-de-descarga)
    - [2.2 Descarga de IDE](#22-descarga-de-ide)
      - [Opción 1: Visual Studio Code (Ligero y rápido)](#opción-1-visual-studio-code-ligero-y-rápido)
      - [Opción 2: Visual Studio Community (Completo y profesional)](#opción-2-visual-studio-community-completo-y-profesional)
  - [3.- Primeros Pasos en C#](#3--primeros-pasos-en-c)
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

## 2.- Ambiente de Trabajo en C#

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

## 3.- Primeros Pasos en C#

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
