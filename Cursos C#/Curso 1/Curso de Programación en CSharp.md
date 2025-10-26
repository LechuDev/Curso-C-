# Curso de Programación en C #

## Introducción

Esta es una recopilación de notas generadas a mano y con ChatGPT, Gemini.
Estas notas fueron tomadas de un curso de programación de YouTube.

Agradezco de antemano al creador de este video

[Curso Programación C# - De Cero a Hero](https://www.youtube.com/watch?v=pTIpUFN1rBY)

Y cualquier persona es libre de Explorar esta información la cual es bastante, asi que dejo a continuación link a el indice, este se abre con

'Ctrl + Click'

Acceso al indice => [Indice](#indice)

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

#### 3.1.1 Versión Antigua (C# 1.0 - 7.0)

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

#### 3.1.2 Versión Moderna (C# 9 y superior)

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

### 5.8 Variables locales y globales

En C#, las **variables** se clasifican según **dónde se declaran** y **qué alcance tienen**: locales o globales. Esto define **dónde puedes acceder a ellas** y **cuánto tiempo viven en memoria**.

---

#### 5.8.1 Variables Locales

- Se declaran **dentro de un método, bloque o función**.
- Solo **existen mientras el método se está ejecutando**.
- No se pueden usar fuera del método donde fueron declaradas.

##### Ejemplo

```csharp
void Saludar()
{
    string mensaje = "Hola desde local"; // Variable local
    Console.WriteLine(mensaje);
}

Saludar();
// Console.WriteLine(mensaje); // ❌ Error: 'mensaje' no existe fuera del método
```

**Explicación:**

- `mensaje` es **local**, solo vive dentro del método `Saludar()`.
- Al salir del método, C# libera la memoria usada por la variable.

---

#### 5.8.2 Variables Globales (Campos / Variables de Clase)

- Se declaran **fuera de cualquier método**, dentro de una clase.
- Son accesibles por **todos los métodos de la misma clase**.
- Permanecen mientras exista el objeto (si son de instancia) o mientras dure la aplicación (si son `static`).

##### Ejemplo de Variables Globales

```csharp
class Persona
{
    public string nombreGlobal = "Lechu"; // Variable global (campo de instancia)
    public static int contador = 0;        // Variable global estática

    public void MostrarNombre()
    {
        Console.WriteLine(nombreGlobal);
    }
}

Persona p = new Persona();
p.MostrarNombre(); // "Lechu"
Console.WriteLine(Persona.contador); // 0
```

**Explicación:**

- `nombreGlobal` → pertenece a cada instancia de la clase `Persona`. Cada objeto tiene su propia copia.
- `contador` → `static`, pertenece a la **clase completa**, no a cada objeto. Se comparte entre todas las instancias.

---

#### 5.8.3 Buenas Prácticas

- **Prefiere variables locales** cuando no necesites que otros métodos accedan a la variable.
- Usa **variables globales** (`static`) solo cuando realmente quieras compartir información entre métodos o instancias.
- Evita abusar de variables globales: pueden generar **errores difíciles de depurar** y confusiones en programas grandes.
- Nombra tus variables de forma clara para saber si son locales o globales (por ejemplo, `nombreGlobal` vs `mensajeLocal`).

---

### 5.9 Variables Privadas y Públicas

En C#, además de **locales y globales**, las variables de clase pueden tener **modificadores de acceso** que determinan **quién puede ver y modificar la variable**:

| Modificador | Qué significa                                                                                |
| ----------- | -------------------------------------------------------------------------------------------- |
| `public`    | La variable **es accesible desde cualquier parte del programa**, incluso desde otras clases. |
| `private`   | La variable **solo es accesible dentro de la clase** donde fue declarada.                    |

---

#### 5.9.1 Variables Públicas (`public`)

- Se declaran con la palabra clave `public`.
- Útiles cuando quieres que otras clases puedan **leer o modificar** el valor directamente.

##### Ejemplo Variables Públicas

```csharp
class Persona
{
    public string nombre; // Variable pública
}

Persona p = new Persona();
p.nombre = "Lechu";
Console.WriteLine(p.nombre); // "Lechu"
```

**Explicación:**

- `nombre` es accesible desde cualquier parte del código.
- Puedes **leer y escribir** su valor directamente.

⚠️ **Advertencia:** Usar demasiadas variables públicas puede ser peligroso porque cualquier clase puede modificarlas, causando errores difíciles de rastrear.

---

#### 5.9.2 Variables Privadas (`private`)

- Se declaran con la palabra clave `private`.
- Solo **los métodos de la misma clase** pueden acceder a ellas.
- Se usan mucho para **ocultar datos** y proteger la integridad del objeto.

##### Ejemplo Variables privadas

```csharp
class Persona
{
    private int edad; // Variable privada

    public void SetEdad(int e)
    {
        if (e >= 0) edad = e; // Validación antes de asignar
    }

    public int GetEdad()
    {
        return edad;
    }
}

Persona p = new Persona();
p.SetEdad(25); 
Console.WriteLine(p.GetEdad()); // 25
// Console.WriteLine(p.edad); // ❌ Error: 'edad' es privada
```

**Explicación:**

- `edad` no puede ser modificada directamente desde fuera.
- Se usan **métodos públicos** (`SetEdad` y `GetEdad`) para **controlar cómo se accede y modifica** la variable.
- Esto se llama **encapsulamiento**, un principio fundamental de la programación orientada a objetos.

---

#### 5.9.3 Buenas Prácticas

- **Prefiere variables privadas** y accede a ellas mediante métodos o propiedades públicas (`get`/`set`).
- Usa variables públicas solo si realmente necesitas que sean **accesibles desde cualquier clase**.
- Encapsular variables ayuda a:

  - Evitar que datos inválidos se asignen.
  - Mejorar la mantenibilidad del código.
  - Facilitar cambios internos sin romper otras partes del programa.

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

## 7.- Los Operadores en C #

Un **operador** es un símbolo que le indica al compilador que realice una operación específica sobre uno o más operandos (valores o variables).

**Ejemplo general:**

```csharp
int a = 10;
int b = 5;
int resultado = a + b; // Usa el operador +
```

En este caso:

- `+` es el **operador**.
- `a` y `b` son los **operandos**.
- `resultado` almacenará la **suma** (15).

C# incluye varios tipos de operadores:

- **Aritméticos** → +, -, *, /, %
- **De asignación** → =, +=, -=, etc.
- **De comparación o relacionales** → ==, !=, >, <, >=, <=
- **Lógicos** → &&, ||, !

---

### 7.1.- Operadores Aritméticos

Esos Operadores siguen una jerarquía de precedencia:

#### 7.1.1.- Suma (`+`)

El operador `+` sirve para **sumar** valores numéricos o **concatenar** strings.

```csharp
int a = 7;
int b = 3;
int suma = a + b;
Console.WriteLine(suma); // 10
```

**También funciona con texto:**

```csharp
string saludo = "Hola " + "mundo!";
Console.WriteLine(saludo); // Hola mundo!
```

---

#### 7.1.2 Resta (`-`)

El operador `-` se usa para **restar** valores o **negar** un número.

```csharp
int a = 10;
int b = 4;
int resta = a - b;
Console.WriteLine(resta); // 6
```

**Negación:**

```csharp
int negativo = -a; // -10
```

---

#### 7.1.3 Multiplicación (`*`)

Multiplica dos valores numéricos.

```csharp
int a = 6;
int b = 4;
int producto = a * b;
Console.WriteLine(producto); // 24
```

💡 *Dato:* También puedes multiplicar variables de tipo `double` o `float` para obtener resultados decimales.

---

#### 7.1.4 División (`/`)

El operador `/` divide dos números.
⚠️ Ten cuidado con los **tipos de datos**, ya que la división entre enteros **descarta los decimales**.

```csharp
int a = 7;
int b = 2;
int division = a / b;
Console.WriteLine(division); // 3 → porque es división entera
```

Si quieres el **resultado decimal**, usa `double` o `float`:

```csharp
double resultado = 7.0 / 2.0;
Console.WriteLine(resultado); // 3.5
```

---

#### 7.1.5 Módulo (`%`)

El operador `%` devuelve el **residuo** (resto) de una división.

```csharp
int a = 10;
int b = 3;
int residuo = a % b;
Console.WriteLine(residuo); // 1
```

💡 *Uso común:* Determinar si un número es **par o impar**:

```csharp
if (a % 2 == 0)
    Console.WriteLine("Es par");
else
    Console.WriteLine("Es impar");
```

---

#### 7.1.6 Incremento (`++`)

Aumenta el valor de una variable **en 1**.
Hay dos formas: **post-incremento** y **pre-incremento**.

```csharp
int x = 5;
x++; // Post-incremento
Console.WriteLine(x); // 6

int y = 5;
++y; // Pre-incremento
Console.WriteLine(y); // 6
```

**Diferencia clave:**

- `x++` → primero usa el valor y luego incrementa.
- `++x` → primero incrementa y luego usa el valor.

---

#### 7.1.7 Decremento (`--`)

Disminuye el valor de una variable **en 1**.
También puede ser **post-decremento** o **pre-decremento**.

```csharp
int z = 10;
z--;
Console.WriteLine(z); // 9
```

---

#### 7.1.8 Exponenciación (potencias)

En C#, **no existe un operador `^` para potencias**, ese símbolo se usa para XOR (operación lógica).
Para elevar un número a una potencia, se usa el método **`Math.Pow()`**.

```csharp
double baseNum = 2;
double exponente = 3;
double resultado = Math.Pow(baseNum, exponente);
Console.WriteLine(resultado); // 8
```

💡 *Dato:* `Math.Pow()` siempre devuelve un **double**.

---

#### 7.1.9 Resumen

| Operador     | Nombre         | Ejemplo          | Resultado  |
| :----------- | :------------- | :--------------- | :--------- |
| `+`          | Suma           | `5 + 3`          | 8          |
| `-`          | Resta          | `5 - 3`          | 2          |
| `*`          | Multiplicación | `5 * 3`          | 15         |
| `/`          | División       | `7 / 2`          | 3 (entero) |
| `%`          | Módulo         | `7 % 2`          | 1          |
| `++`         | Incremento     | `x++`            | x = x + 1  |
| `--`         | Decremento     | `x--`            | x = x - 1  |
| `Math.Pow()` | Exponenciación | `Math.Pow(2, 3)` | 8          |

---

#### 7.1.10 Ejemplo: Calculadora simple

Aquí tienes un ejemplo completo que muestra todos los operadores en acción:

```csharp
using System;

class Calculadora
{
    static void Main()
    {
        double a = 10, b = 3;

        Console.WriteLine($"Suma: {a + b}");
        Console.WriteLine($"Resta: {a - b}");
        Console.WriteLine($"Multiplicación: {a * b}");
        Console.WriteLine($"División: {a / b}");
        Console.WriteLine($"Módulo: {a % b}");
        Console.WriteLine($"Incremento de a: {++a}");
        Console.WriteLine($"Decremento de b: {--b}");
        Console.WriteLine($"Potencia: {Math.Pow(2, 5)}");
    }
}
```

**Salida:**

```console
Suma: 13
Resta: 7
Multiplicación: 30
División: 3.3333333333333335
Módulo: 1
Incremento de a: 11
Decremento de b: 2
Potencia: 32
```

---

💡 **Consejo final:**
Practica cada operador con distintos tipos de datos (`int`, `double`, `float`, `decimal`) para entender cómo C# maneja las conversiones y los resultados.

---

### 7.2.- Operadores de Asignación

Los **operadores de asignación** se utilizan para **asignar valores a variables** y, en muchos casos, **combinar operaciones aritméticas con asignación** en un solo paso.

---

#### 🔹 7.2.1 Asignación básica (`=`)

El operador `=` asigna el valor de la derecha a la variable de la izquierda.

```csharp
int a = 10;  // La variable 'a' recibe el valor 10
Console.WriteLine(a); // 10
```

**Explicación:**

1. `int a` → Declara una variable de tipo entero.
2. `= 10` → Asigna el valor 10 a `a`.
3. `Console.WriteLine(a)` → Imprime el valor actual de `a`.

---

#### 🔹 7.2.2 Asignación con suma (`+=`)

Suma un valor a la variable **y guarda el resultado en la misma variable**.

```csharp
int a = 5;
a += 3;  // Equivalente a: a = a + 3
Console.WriteLine(a); // 8
```

**Explicación paso a paso:**

- `a += 3` → toma el valor actual de `a` (5), le suma 3, y guarda 8 de nuevo en `a`.

---

#### 🔹 7.2.3 Asignación con resta (`-=`)

Resta un valor a la variable y guarda el resultado.

```csharp
int a = 10;
a -= 4;  // Equivalente a: a = a - 4
Console.WriteLine(a); // 6
```

---

#### 🔹 7.2.4 Asignación con multiplicación (`*=`)

Multiplica el valor de la variable por un número y lo guarda.

```csharp
int a = 7;
a *= 3;  // a = a * 3
Console.WriteLine(a); // 21
```

---

#### 🔹 7.2.5 Asignación con división (`/=`)

Divide la variable por un valor y guarda el resultado.
⚠️ Recuerda el comportamiento de los tipos de datos (`int` vs `double`).

```csharp
double a = 15;
a /= 4;  // a = a / 4
Console.WriteLine(a); // 3.75
```

---

#### 🔹 7.2.6 Asignación con módulo (`%=`)

Calcula el residuo de la división y lo asigna a la variable.

```csharp
int a = 10;
a %= 3;  // a = a % 3
Console.WriteLine(a); // 1
```

---

#### 🔹 7.2.7 Resumen de los operadores de asignación

| Operador | Equivalente | Descripción         |
| :------- | :---------- | :------------------ |
| `=`      | `a = b`     | Asignación simple   |
| `+=`     | `a = a + b` | Suma y asigna       |
| `-=`     | `a = a - b` | Resta y asigna      |
| `*=`     | `a = a * b` | Multiplica y asigna |
| `/=`     | `a = a / b` | Divide y asigna     |
| `%=`     | `a = a % b` | Módulo y asigna     |

---

💡 **Consejos prácticos:**

- Usa operadores compuestos (`+=`, `-=`, etc.) para **código más limpio y legible**.
- Son especialmente útiles en **bucles**, contadores y acumuladores:

```csharp
int suma = 0;
for(int i = 1; i <= 5; i++)
{
    suma += i; // Acumula los valores del 1 al 5
}
Console.WriteLine(suma); // 15
```

#### 🔹 7.2.8 Ejemplo: Calculadora avanzada

Este ejemplo muestra cómo usar **operadores aritméticos**, **asignación** y **combinación de operaciones** en un programa simple tipo calculadora:

```csharp
using System;

class CalculadoraAvanzada
{
    static void Main()
    {
        // Declaración de variables
        double numero1 = 15;
        double numero2 = 4;

        // Operaciones básicas
        double suma = numero1 + numero2;
        double resta = numero1 - numero2;
        double multiplicacion = numero1 * numero2;
        double division = numero1 / numero2;
        double modulo = numero1 % numero2;

        Console.WriteLine($"Suma: {suma}");
        Console.WriteLine($"Resta: {resta}");
        Console.WriteLine($"Multiplicación: {multiplicacion}");
        Console.WriteLine($"División: {division}");
        Console.WriteLine($"Módulo: {modulo}");

        // Uso de operadores de asignación compuesta
        double valor = 10;
        valor += 5;  // valor = valor + 5
        Console.WriteLine($"Valor después de += 5: {valor}");

        valor *= 2;  // valor = valor * 2
        Console.WriteLine($"Valor después de *= 2: {valor}");

        valor -= 4;  // valor = valor - 4
        Console.WriteLine($"Valor después de -= 4: {valor}");

        valor /= 3;  // valor = valor / 3
        Console.WriteLine($"Valor después de /= 3: {valor}");

        valor %= 2;  // valor = valor % 2
        Console.WriteLine($"Valor después de %= 2: {valor}");

        // Exponenciación usando Math.Pow
        double potencia = Math.Pow(numero1, 2); // numero1^2
        Console.WriteLine($"Potencia: {potencia}");
    }
}
```

---

##### 🔹 Explicación paso a paso

1. **Declaración de variables:**

   - `numero1` y `numero2` se usan para operaciones básicas.
   - `valor` se usa para mostrar **operadores de asignación compuesta**.

2. **Operaciones aritméticas:**

   - `+`, `-`, `*`, `/`, `%` → realizan suma, resta, multiplicación, división y módulo.

3. **Operadores de asignación compuesta:**

   - `+=, -=, *=, /=, %=` → simplifican el código combinando operación y asignación.
   - El valor de `valor` se actualiza paso a paso mostrando cada resultado.

4. **Exponenciación:**

   - `Math.Pow(numero1, 2)` → eleva `numero1` al cuadrado.
   - Siempre devuelve un `double`.

---

**Salida del programa:**

```yaml
Suma: 19
Resta: 11
Multiplicación: 60
División: 3.75
Módulo: 3
Valor después de += 5: 15
Valor después de *= 2: 30
Valor después de -= 4: 26
Valor después de /= 3: 8.666666666666666
Valor después de %= 2: 0.666666666666666
Potencia: 225
```

---

💡 **Consejos:**

- Este ejemplo combina **todos los operadores vistos hasta ahora** en un solo programa.
- Ideal para practicar cómo se **actualizan variables paso a paso** y cómo funcionan los operadores de **asignación compuesta** y **aritmética** juntos.
- Puedes modificar los valores de `numero1` y `numero2` para probar distintos escenarios.

---

### 7.3.- Operadores Relacionales y de Comparación

Los **operadores relacionales** se usan para **comparar valores**.
Siempre devuelven un valor **booleano** (`true` o `false`).
Son fundamentales para **condicionales** (`if`, `while`) y **bucles**.

---

#### 🔹 7.3.1 Igualdad (`==`)

Comprueba si dos valores son iguales.

```csharp
int a = 5;
int b = 5;
bool resultado = a == b; // true
Console.WriteLine(resultado);
```

**Explicación:**

- `==` compara los valores de `a` y `b`.
- Si son iguales, devuelve `true`; si no, `false`.

---

#### 🔹 7.3.2 Diferente (`!=`)

Comprueba si dos valores **no son iguales**.

```csharp
int a = 5;
int b = 3;
bool resultado = a != b; // true
Console.WriteLine(resultado);
```

---

#### 🔹 7.3.3 Mayor que (`>`)

Comprueba si un valor es **mayor que** otro.

```csharp
int a = 10;
int b = 7;
bool resultado = a > b; // true
Console.WriteLine(resultado);
```

---

#### 🔹 7.3.4 Menor que (`<`)

Comprueba si un valor es **menor que** otro.

```csharp
int a = 10;
int b = 15;
bool resultado = a < b; // true
Console.WriteLine(resultado);
```

---

#### 🔹 7.3.5 Mayor o igual que (`>=`)

Comprueba si un valor es **mayor o igual** que otro.

```csharp
int a = 10;
int b = 10;
bool resultado = a >= b; // true
Console.WriteLine(resultado);
```

---

#### 🔹 7.3.6 Menor o igual que (`<=`)

Comprueba si un valor es **menor o igual** que otro.

```csharp
int a = 7;
int b = 10;
bool resultado = a <= b; // true
Console.WriteLine(resultado);
```

---

#### 🔹 7.3.7 Ejemplo práctico: Comparaciones combinadas

```csharp
int edad = 25;
int edadMinima = 18;
int edadMaxima = 30;

// Verifica si la edad está dentro del rango
bool permitido = (edad >= edadMinima) && (edad <= edadMaxima);
Console.WriteLine($"Edad dentro del rango: {permitido}"); // true

// Verifica si la edad no está en el rango
bool fueraRango = (edad < edadMinima) || (edad > edadMaxima);
Console.WriteLine($"Edad fuera del rango: {fueraRango}"); // false
```

**Explicación paso a paso:**

1. `(edad >= edadMinima)` → `true` si la persona cumple la edad mínima.
2. `(edad <= edadMaxima)` → `true` si la persona cumple la edad máxima.
3. `&&` → operador lógico que devuelve `true` solo si ambas condiciones son `true`.
4. `||` → operador lógico que devuelve `true` si **al menos una** de las condiciones es `true`.

---

💡 **Resumen visual de los operadores relacionales:**

| Operador | Significado       |
| -------- | ----------------- |
| `==`     | Igual a           |
| `!=`     | Distinto de       |
| `>`      | Mayor que         |
| `<`      | Menor que         |
| `>=`     | Mayor o igual que |
| `<=`     | Menor o igual que |

---

### 7.4.- Operadores Lógicos (`&&`, `||`, `!`)

Los **operadores lógicos** se usan para **combinar o invertir expresiones booleanas** (`true` o `false`).
Son fundamentales cuando necesitamos evaluar **más de una condición** al mismo tiempo.

---

#### 🔹 7.4.1 AND lógico (`&&`)

El operador **AND (`&&`)** devuelve `true` **solo si ambas condiciones son verdaderas**.

```csharp
int edad = 25;
bool tieneLicencia = true;

// Verifica si cumple edad y tiene licencia
bool puedeConducir = (edad >= 18) && tieneLicencia;
Console.WriteLine(puedeConducir); // true
```

**Explicación paso a paso:**

1. `(edad >= 18)` → `true` porque 25 >= 18
2. `tieneLicencia` → `true`
3. `&&` combina las dos condiciones: `true && true` → `true`

Si alguna condición fuera `false`, el resultado sería `false`.

💡 *Tip:* AND lógico es útil cuando todas las condiciones **deben cumplirse simultáneamente**.

---

#### 🔹 7.4.2 OR lógico (`||`)

El operador **OR (`||`)** devuelve `true` **si al menos una condición es verdadera**.

```csharp
bool tieneLlaves = false;
bool conoceCodigo = true;

// Puede abrir la puerta si tiene llaves o conoce el código
bool puedeEntrar = tieneLlaves || conoceCodigo;
Console.WriteLine(puedeEntrar); // true
```

**Explicación paso a paso:**

1. `tieneLlaves` → `false`
2. `conoceCodigo` → `true`
3. `||` combina las condiciones: `false || true` → `true`

💡 *Tip:* OR lógico se usa cuando basta **cumplir una de varias condiciones**.

---

#### 🔹 7.4.3 NOT lógico (`!`)

El operador **NOT (`!`)** invierte el valor de una expresión booleana.

```csharp
bool estaLloviendo = true;
bool noLlueve = !estaLloviendo;
Console.WriteLine(noLlueve); // false
```

**Explicación:**

- `!estaLloviendo` invierte `true` → `false`.
- Es útil para condiciones de **negación** en `if`.

---

#### 🔹 7.4.4 Combinación de operadores lógicos y relacionales

Generalmente, los operadores lógicos se usan **junto con operadores relacionales** para crear condiciones más complejas.

```csharp
int edad = 20;
double saldo = 500.0;

// Requisitos: edad entre 18 y 30, o saldo mayor a 1000
bool puedeAcceder = ((edad >= 18 && edad <= 30) || saldo > 1000);
Console.WriteLine(puedeAcceder); // true
```

**Explicación paso a paso:**

1. `(edad >= 18 && edad <= 30)` → `true && true` → `true`
2. `saldo > 1000` → `500 > 1000` → `false`
3. `(true || false)` → `true`

> ⚡ *Tip:* Usa paréntesis para controlar el orden de evaluación.
> En C#, `&&` tiene mayor prioridad que `||`.

---

#### 🔹 7.4.5 Tabla de verdad de operadores lógicos

**AND (`&&`)**

| A     | B     | A && B |
| ----- | ----- | ------ |
| true  | true  | true   |
| true  | false | false  |
| false | true  | false  |
| false | false | false  |

**OR (`||`)**

| A     | B     | A || B |
|-------|-------|--------|
| true  | true  | true   |
| true  | false | true   |
| false | true  | true   |
| false | false | false  |

**NOT (`!`)**

| A     | !A    |
| ----- | ----- |
| true  | false |
| false | true  |

---

#### 🔹 7.4.6 Ejemplo práctico: Control de acceso

```csharp
string usuario = "admin";
string password = "1234";
bool esAdmin = (usuario == "admin") && (password == "1234");

if (esAdmin)
{
    Console.WriteLine("Acceso concedido");
}
else
{
    Console.WriteLine("Acceso denegado");
}
```

**Explicación:**

1. `(usuario == "admin")` → verifica igualdad
2. `(password == "1234")` → verifica igualdad
3. `&&` → ambas condiciones deben cumplirse para dar acceso.
4. `if` evalúa el resultado booleano y decide la acción.

---

💡 **Consejos prácticos:**

- Combina operadores relacionales y lógicos para condiciones complejas.
- Siempre usa paréntesis para dejar claro **el orden de evaluación**.
- Los operadores lógicos se usan mucho en **bucles y validaciones**: login, formularios, juegos, etc.

---

¡Perfecto! Vamos a crear un **ejemplo completo de calculadora avanzada en C#** que combine **todos los operadores vistos hasta ahora**: aritméticos, de asignación, relacionales y lógicos. La idea es que veas cómo se usan juntos en un solo programa práctico y comentado paso a paso. 😎

---

### 7.6.- Operador de Incremento (`++`)

El operador **incremento (`++`)** aumenta **en 1** el valor de una variable.
Se puede usar de **dos formas**:

1. **Prefijo:** `++variable` → primero incrementa, luego usa el valor.
2. **Sufijo:** `variable++` → primero usa el valor, luego incrementa.

---

#### 🔹 Ejemplo 1: Prefijo (`++variable`)

```csharp
int numero = 5;
int resultado = ++numero; // Primero incrementa, luego asigna
Console.WriteLine($"numero: {numero}");     // 6
Console.WriteLine($"resultado: {resultado}"); // 6
```

**Explicación:**

- `++numero` incrementa `numero` a 6 **antes** de asignarlo a `resultado`.
- Ambos, `numero` y `resultado`, valen 6.

---

#### 🔹 Ejemplo 2: Sufijo (`variable++`)

```csharp
int numero = 5;
int resultado = numero++; // Primero asigna, luego incrementa
Console.WriteLine($"numero: {numero}");     // 6
Console.WriteLine($"resultado: {resultado}"); // 5
```

**Explicación:**

- `numero++` primero asigna el valor actual de `numero` a `resultado` (5).
- Luego incrementa `numero` a 6.

💡 *Tip:* Prefijo se usa cuando necesitas el valor incrementado inmediatamente.
Sufijo se usa cuando quieres usar el valor actual antes de incrementarlo.

---

### 7.7.- Operador de Decremento (`--`)

El operador **decremento (`--`)** disminuye **en 1** el valor de una variable.
También tiene **prefijo y sufijo**.

---

#### 🔹 Ejemplo 1: Prefijo (`--variable`)

```csharp
int numero = 5;
int resultado = --numero; // Primero decrementa, luego asigna
Console.WriteLine($"numero: {numero}");     // 4
Console.WriteLine($"resultado: {resultado}"); // 4
```

---

#### 🔹 Ejemplo 2: Sufijo (`variable--`)

```csharp
int numero = 5;
int resultado = numero--; // Primero asigna, luego decrementa
Console.WriteLine($"numero: {numero}");     // 4
Console.WriteLine($"resultado: {resultado}"); // 5
```

---

### 7.8.- Exponenciación (`Math.Pow`)

En C#, **no existe un operador `^` para potencia** como en algunos otros lenguajes.
En su lugar, se utiliza el método **`Math.Pow(base, exponente)`**, que devuelve un **double**.

---

#### 7.8.1.-🔹 Ejemplo básico de `Math.Pow`

```csharp
double baseNumero = 3;
double exponente = 4;

double resultado = Math.Pow(baseNumero, exponente); // 3^4
Console.WriteLine($"Resultado: {resultado}"); // 81
```

**Explicación paso a paso:**

1. `Math.Pow(3, 4)` → calcula (3^4 = 3 *3* 3 * 3 = 81)
2. Siempre devuelve un tipo **double**, aunque la base y el exponente sean enteros.
3. Se puede usar con variables y expresiones directamente.

---

#### 7.8.2.-🔹 Combinación con otros operadores

```csharp
double a = 2;
double b = 5;
double c = 3;

// Operación combinada: ((a^b) + c) / 2
double resultado = (Math.Pow(a, b) + c) / 2;
Console.WriteLine($"Resultado combinado: {resultado}");
```

**Explicación:**

1. `Math.Pow(a, b)` → (2^5 = 32)
2. `32 + c` → `32 + 3 = 35`
3. `35 / 2` → `17.5`

> Esto muestra cómo **integrar exponenciación en expresiones aritméticas complejas**.

---

#### 7.8.3🔹 Ejemplo avanzado: Validación de resultados

Supongamos que queremos **verificar si un número elevado a una potencia supera cierto límite**:

```csharp
double baseNumero = 4;
double exponente = 3;
double limite = 60;

double potencia = Math.Pow(baseNumero, exponente);

bool dentroDelLimite = potencia <= limite;  // Operador relacional
bool permitido = dentroDelLimite && (baseNumero > 0); // Operador lógico

Console.WriteLine($"Potencia: {potencia}");             // 64
Console.WriteLine($"Dentro del límite: {dentroDelLimite}"); // false
Console.WriteLine($"Permitido: {permitido}");          // false
```

**Explicación:**

1. `Math.Pow(4, 3)` → 64
2. `64 <= 60` → `false`
3. `(false) && (4 > 0)` → `false`
4. Demuestra cómo combinar **exponenciación, relacionales y lógicos** en un mismo cálculo.

---

#### 7.8.4🔹 Resumen

- `Math.Pow(base, exponente)` → calcula la potencia.
- Siempre devuelve `double`.
- Se puede combinar con **operadores aritméticos** (`+`, `-`, `*`, `/`, `%`) y **relacionales/lógicos** para condicionales.
- Ideal para cálculos matemáticos, validaciones, simulaciones y juegos.

---

### 7.9.- Ejemplo final: Calculadora Avanzada

```csharp
using System;

class CalculadoraAvanzada
{
    static void Main()
    {
        // --- Declaración de variables ---
        double num1 = 10;
        double num2 = 3;
        double resultado;

        Console.WriteLine("=== Calculadora Avanzada ===");

        // --- Operaciones aritméticas ---
        resultado = num1 + num2;
        Console.WriteLine($"Suma: {num1} + {num2} = {resultado}");

        resultado = num1 - num2;
        Console.WriteLine($"Resta: {num1} - {num2} = {resultado}");

        resultado = num1 * num2;
        Console.WriteLine($"Multiplicación: {num1} * {num2} = {resultado}");

        resultado = num1 / num2;
        Console.WriteLine($"División: {num1} / {num2} = {resultado}");

        resultado = num1 % num2;
        Console.WriteLine($"Módulo: {num1} % {num2} = {resultado}");

        resultado = Math.Pow(num1, num2);
        Console.WriteLine($"Potencia: {num1}^{num2} = {resultado}");

        // --- Operadores de asignación compuesta ---
        double valor = 5;
        valor += 2; // valor = 7
        valor *= 3; // valor = 21
        valor -= 4; // valor = 17
        valor /= 2; // valor = 8.5
        valor %= 3; // valor = 2.5
        Console.WriteLine($"Valor final con asignación compuesta: {valor}");

        // --- Incremento y decremento ---
        int a = 5;
        Console.WriteLine($"a antes del incremento: {a}");
        Console.WriteLine($"Prefijo ++a: {++a}"); // 6
        Console.WriteLine($"Sufijo a++: {a++}");  // muestra 6, luego a = 7
        Console.WriteLine($"a después del sufijo: {a}");
        
        int b = 10;
        Console.WriteLine($"Prefijo --b: {--b}"); // 9
        Console.WriteLine($"Sufijo b--: {b--}");  // muestra 9, luego b = 8
        Console.WriteLine($"b después del sufijo: {b}");

        // --- Operadores relacionales ---
        bool mayor = num1 > num2;
        bool igual = num1 == num2;
        bool menorIgual = num1 <= num2;
        Console.WriteLine($"num1 > num2: {mayor}");
        Console.WriteLine($"num1 == num2: {igual}");
        Console.WriteLine($"num1 <= num2: {menorIgual}");

        // --- Operadores lógicos ---
        bool cond1 = (num1 > 0) && (num2 > 0); // AND
        bool cond2 = (num1 < 0) || (num2 > 0); // OR
        bool cond3 = !(num1 == num2);          // NOT
        Console.WriteLine($"(num1 > 0) && (num2 > 0): {cond1}");
        Console.WriteLine($"(num1 < 0) || (num2 > 0): {cond2}");
        Console.WriteLine($"!(num1 == num2): {cond3}");

        // --- Ejemplo combinado: validación avanzada ---
        if ((num1 > num2 && num2 != 0) || (Math.Pow(num1, 2) > 50))
        {
            Console.WriteLine("Condición avanzada cumplida");
        }
        else
        {
            Console.WriteLine("Condición avanzada NO cumplida");
        }

        Console.WriteLine("=== Fin de la Calculadora Avanzada ===");
    }
}
```

---

#### 🔹 7.9.1 Explicación paso a paso

1. **Aritméticos:** `+`, `-`, `*`, `/`, `%`, `Math.Pow()` → operaciones básicas y potencia.
2. **Asignación compuesta:** `+=, *=, -=, /=, %=` → actualiza variable paso a paso.
3. **Incremento/decremento:** `++a, a++, --b, b--` → prefijo y sufijo.
4. **Relacionales:** `>`, `==`, `<=` → comparaciones para condiciones booleanas.
5. **Lógicos:** `&&`, `||`, `!` → combinación de condiciones booleanas.
6. **Ejemplo combinado final:** `if ((num1 > num2 && num2 != 0) || (Math.Pow(num1,2) > 50))`
   → demuestra cómo todos los operadores trabajan juntos en un escenario real.

---

💡 **Salida esperada (aproximada):**

```yaml
=== Calculadora Avanzada ===
Suma: 10 + 3 = 13
Resta: 10 - 3 = 7
Multiplicación: 10 * 3 = 30
División: 10 / 3 = 3.3333333333333335
Módulo: 10 % 3 = 1
Potencia: 10^3 = 1000
Valor final con asignación compuesta: 2.5
a antes del incremento: 5
Prefijo ++a: 6
Sufijo a++: 6
a después del sufijo: 7
Prefijo --b: 9
Sufijo b--: 9
b después del sufijo: 8
num1 > num2: True
num1 == num2: False
num1 <= num2: False
(num1 > 0) && (num2 > 0): True
(num1 < 0) || (num2 > 0): True
!(num1 == num2): True
Condición avanzada cumplida
=== Fin de la Calculadora Avanzada ===
```

---

## 8.- Transformar Cadenas a Valores Numéricos

En programación, es común recibir **datos en forma de texto** (strings) que necesitamos **convertir a números** para poder realizar operaciones matemáticas o comparaciones. C# ofrece varias formas de hacerlo de manera segura y eficiente.

---

### 8.1.- Conversión usando `int.Parse()` y `double.Parse()`

- `int.Parse(string)` → convierte un string a **entero** (`int`).
- `double.Parse(string)` → convierte un string a **decimal** o número con decimales (`double`).

**Ejemplo:**

```csharp
string textoEntero = "42";
string textoDecimal = "3.14";

int numeroEntero = int.Parse(textoEntero);
double numeroDecimal = double.Parse(textoDecimal);

Console.WriteLine($"Entero: {numeroEntero}");
Console.WriteLine($"Decimal: {numeroDecimal}");
```

**Salida:**

```yaml
Entero: 42
Decimal: 3.14
```

**Nota:**
Si el texto no representa un número válido, `Parse()` lanzará una **excepción** (`FormatException`).

---

### 8.2.- Conversión segura con `TryParse()`

`TryParse()` permite convertir cadenas sin riesgo de excepción. Devuelve un **booleano** indicando si la conversión fue exitosa.

**Sintaxis:**

```csharp
int resultadoEntero;
bool exito = int.TryParse("123", out resultadoEntero);

if (exito)
    Console.WriteLine($"Conversión exitosa: {resultadoEntero}");
else
    Console.WriteLine("No se pudo convertir la cadena");
```

**Ventajas:**

- Evita errores de ejecución.
- Útil cuando el usuario ingresa datos que pueden no ser numéricos.

---

### 8.3.- Conversión de números decimales

```csharp
double resultadoDecimal;
if (double.TryParse("12.34", out resultadoDecimal))
{
    Console.WriteLine($"Número decimal: {resultadoDecimal}");
}
else
{
    Console.WriteLine("Error al convertir a decimal");
}
```

**Tip:** Para configuraciones de región donde el separador decimal es coma `,`, se puede usar `CultureInfo.InvariantCulture`:

```csharp
using System.Globalization;

double numero = double.Parse("12.34", CultureInfo.InvariantCulture);
```

---

### 8.4.- Conversión usando `Convert.ToInt32()` y `Convert.ToDouble()`

- Otra alternativa segura que convierte y devuelve un número.
- Devuelve **0** si la cadena es `null`, pero lanzará excepción si el formato es incorrecto.

```csharp
string texto = "56";
int numero = Convert.ToInt32(texto);
Console.WriteLine(numero); // 56
```

---

### 8.5.- Conversión a otros tipos numéricos con `Convert`

C# ofrece el **namespace `System`** con la clase `Convert`, que permite transformar strings u otros tipos en diferentes tipos numéricos de forma sencilla:

```csharp
string textoFloat = "3.14";
string textoDecimal = "12.3456";
string textoLong = "9876543210";

// Convertir a float (Single)
float numeroFloat = Convert.ToSingle(textoFloat);
Console.WriteLine($"float: {numeroFloat}");

// Convertir a decimal
decimal numeroDecimal = Convert.ToDecimal(textoDecimal);
Console.WriteLine($"decimal: {numeroDecimal}");

// Convertir a long (Int64)
long numeroLong = Convert.ToInt64(textoLong);
Console.WriteLine($"long: {numeroLong}");
```

**Salida esperada:**

```yaml
float: 3.14
decimal: 12.3456
long: 9876543210
```

---

### 8.6.-Tabla de Conversiones en C #

| Valor de ejemplo         | Tipo Origen | Tipo Destino | Método / Función      | Tipo resultante | Comentario                                          |
| ------------------------ | ----------- | ------------ | --------------------- | --------------- | --------------------------------------------------- |
| `"42"`                   | string      | int          | `int.Parse()`         | int             | Lanza excepción si no es numérico                   |
| `"3.1416"`               | string      | double       | `double.Parse()`      | double          | Lanza excepción si no es numérico                   |
| `"42"`                   | string      | int          | `int.TryParse()`      | int             | Seguro: devuelve true/false y valor en `out`        |
| `"3.1416"`               | string      | double       | `double.TryParse()`   | double          | Seguro: devuelve true/false y valor en `out`        |
| `"42"`                   | string      | int          | `Convert.ToInt32()`   | int             | Convierte null a 0, lanza error si formato inválido |
| `"3.1416"`               | string      | double       | `Convert.ToDouble()`  | double          | Convierte null a 0, lanza error si formato inválido |
| `"2.718"`                | string      | float        | `Convert.ToSingle()`  | float           | Convierte string a float (Single precision)         |
| `"3.1416"`               | string      | decimal      | `Convert.ToDecimal()` | decimal         | Alta precisión para cálculos financieros            |
| `"9876543210"`           | string      | long         | `Convert.ToInt64()`   | long            | Para enteros grandes de 64 bits                     |
| `"255"`                  | string      | byte         | `Convert.ToByte()`    | byte            | Convierte string a byte (0-255)                     |
| `"127"`                  | string      | sbyte        | `Convert.ToSByte()`   | sbyte           | Convierte string a sbyte (-128 a 127)               |
| `"4294967295"`           | string      | uint         | `Convert.ToUInt32()`  | uint            | Convierte string a entero sin signo 32 bits         |
| `"18446744073709551615"` | string      | ulong        | `Convert.ToUInt64()`  | ulong           | Convierte string a entero sin signo 64 bits         |

---

💡 **Notas:**

1. **`Parse()`** → es rápido pero **arriesgado** si el string no es numérico; pero **lanza excepción si el formato es inválido**.
2. **`TryParse()`** → es **seguro** y recomendado cuando la entrada puede ser inválida., devuelve booleano indicando si la conversión fue exitosa y el valor convertido en `out`.
3. **`Convert.ToX()`** → maneja **nulls**, pero no strings inválidas y convierte entre tipos, pero aún puede lanzar excepción si el formato es inválido  lanzará **`FormatException`**..
4. Tipos `float`, `double`, `decimal` → se usan según precisión requerida.
5. Tipos `byte`, `sbyte`, `uint`, `ulong` → útiles para optimización de memoria o rangos específicos de valores.
6. Para **decimal/floating point**, se puede usar `CultureInfo.InvariantCulture` si el separador decimal puede variar.

## 9.- Funciones Matemáticas de la Librería Math

En C#, la **clase `Math`** del **namespace `System`** ofrece un conjunto completo de **funciones matemáticas** para realizar operaciones comunes y avanzadas. Estas funciones permiten:

- Calcular raíces, potencias y logaritmos.
- Redondear números.
- Trabajar con trigonometría.
- Obtener valores absolutos y comparaciones entre números.

Todas las funciones de `Math` son **estáticas**, lo que significa que no necesitas crear una instancia de la clase para usarlas. Por ejemplo:

```csharp
double resultado = Math.Sqrt(16); // Devuelve 4
```

---

### 9.1.- Raíz Cuadrada y Potencias

1. **`Math.Sqrt(double x)`** → Devuelve la raíz cuadrada de un número.

```csharp
double raiz = Math.Sqrt(25); // 5
```

2. **`Math.Pow(double x, double y)`** → Eleva `x` a la potencia `y`.

```csharp
double potencia = Math.Pow(2, 3); // 8
```

---

### 9.2.- Valores Absolutos y Signos

3. **`Math.Abs(double x)`** → Devuelve el valor absoluto de un número.

```csharp
double absoluto = Math.Abs(-10); // 10
```

4. **`Math.Sign(double x)`** → Devuelve -1, 0 o 1 dependiendo del signo del número.

```csharp
int signo = Math.Sign(-15); // -1
```

---

### 9.3.- Redondeo y Truncamiento

5. **`Math.Round(double x)`** → Redondea al número entero más cercano.

```csharp
double redondeo = Math.Round(3.6); // 4
```

6. **`Math.Ceiling(double x)`** → Redondea hacia arriba (techo).

```csharp
double techo = Math.Ceiling(3.2); // 4
```

7. **`Math.Floor(double x)`** → Redondea hacia abajo (piso).

```csharp
double piso = Math.Floor(3.8); // 3
```

8. **`Math.Truncate(double x)`** → Elimina la parte decimal sin redondear.

```csharp
double truncado = Math.Truncate(3.9); // 3
```

---

### 9.4.- Mínimo, Máximo y Comparaciones

9. **`Math.Min(double a, double b)`** → Devuelve el menor de dos números.

```csharp
double menor = Math.Min(5, 9); // 5
```

10. **`Math.Max(double a, double b)`** → Devuelve el mayor de dos números.

```csharp
double mayor = Math.Max(5, 9); // 9
```

---

### 9.5.- Logaritmos y Exponenciales

11. **`Math.Exp(double x)`** → Devuelve `e` elevado a `x`.

```csharp
double eElevado = Math.Exp(1); // 2.718281828...
```

12. **`Math.Log(double x)`** → Logaritmo natural (base e) de `x`.

```csharp
double log = Math.Log(7.389); // ~2
```

13. **`Math.Log10(double x)`** → Logaritmo en base 10 de `x`.

```csharp
double log10 = Math.Log10(1000); // 3
```

---

### 9.6.- Trigonometría

14. **`Math.Sin(double x)`** → Seno de `x` (en radianes).

```csharp
double seno = Math.Sin(Math.PI / 2); // 1
```

15. **`Math.Cos(double x)`** → Coseno de `x` (en radianes).

```csharp
double coseno = Math.Cos(0); // 1
```

16. **`Math.Tan(double x)`** → Tangente de `x` (en radianes).

```csharp
double tangente = Math.Tan(Math.PI / 4); // ~1
```

---

### 9.8.- Raíces y Potencias Avanzadas

21. **`Math.Cbrt(double x)`** → Calcula la raíz cúbica de un número (disponible en C# 8 y superior).

```csharp
double raizCubica = Math.Cbrt(27); // 3
```

22. **`Math.Pow(x, 1.0 / n)`** → Para calcular raíces n-ésimas si `Cbrt()` no está disponible.

```csharp
double raizCuarta = Math.Pow(16, 0.25); // 2
```

---

### 9.9.- Funciones de Redondeo con Decimales

23. **`Math.Round(double x, int decimals)`** → Redondea `x` a `decimals` cifras decimales.

```csharp
double redondeoDecimal = Math.Round(3.14159, 2); // 3.14
```

24. **`Math.Floor()` y `Math.Ceiling()`** combinadas con multiplicación para redondeos específicos:

```csharp
double valor = 5.67;
double redondearAlEnteroMasCercano = Math.Floor(valor + 0.5); // 6
```

---

### 9.10.- Funciones de Valor Absoluto Avanzadas

25. **`Math.Abs(decimal x)`** → Valor absoluto para tipo decimal.
26. **`Math.Abs(int x)`** → Valor absoluto para enteros.
27. **`Math.Abs(float x)`** → Valor absoluto para float.
28. **`Math.Abs(long x)`** → Valor absoluto para long.

> Nota: `Math.Abs()` es **sobrecargada** para diferentes tipos numéricos.

---

### 9.11.- Comparaciones y Clamping

29. **`Math.Clamp(double value, double min, double max)`** → Restringe un valor a un rango `[min, max]`.

```csharp
double valor = 12;
double valorClampeado = Math.Clamp(valor, 0, 10); // 10
```

30. **`Math.Max()` y `Math.Min()`** → Para comparaciones rápidas entre dos valores (ya visto).

---

### 9.12.- Funciones Trigonométricas Adicionales

31. **`Math.Asin(double x)`** → Arco seno (devuelve radianes).

```csharp
double asin = Math.Asin(1); // PI/2
```

32. **`Math.Acos(double x)`** → Arco coseno.

33. **`Math.Atan(double x)`** → Arco tangente.

34. **`Math.Atan2(double y, double x)`** → Arco tangente considerando ambos ejes para obtener ángulo completo.

---

### 9.13.- Funciones Hiperbólicas

35. **`Math.Sinh(double x)`** → Seno hiperbólico.
36. **`Math.Cosh(double x)`** → Coseno hiperbólico.
37. **`Math.Tanh(double x)`** → Tangente hiperbólica.

---

### 9.14.- Funciones de Comparación de Precisión

38. **`Math.IEEERemainder(double x, double y)`** → Devuelve el residuo de la división de acuerdo a la norma IEEE 754.

---

💡 **Tip General:**

- La clase `Math` es **estática**, por lo que se llama como `Math.Funcion()`.
- Muchas funciones aceptan `double`, pero hay **sobrecargas** para `int`, `long`, `float`, `decimal`.
- Se recomienda **usar `Math.Round` o `Math.Truncate`** para resultados controlados cuando trabajes con decimales.

---

### 9.15.- Ejemplo práctico: “Demostración completa de Math”

```csharp
using System;

class DemoMath
{
    static void Main()
    {
        Console.WriteLine("=== Funciones Matemáticas de la clase Math ===\n");

        double valor = 9;
        double valor2 = 2.5;
        double angulo = Math.PI / 4; // 45 grados

        // --- Raíces y Potencias ---
        Console.WriteLine($"Raíz cuadrada de {valor}: {Math.Sqrt(valor)}");
        Console.WriteLine($"{valor} elevado a 3: {Math.Pow(valor, 3)}");
        Console.WriteLine($"Raíz cúbica de 27: {Math.Cbrt(27)}");

        // --- Valores Absolutos ---
        Console.WriteLine($"Valor absoluto de -15: {Math.Abs(-15)}");

        // --- Redondeos ---
        Console.WriteLine($"Redondeo de 2.5: {Math.Round(valor2)}");
        Console.WriteLine($"Redondeo a 1 decimal de 2.567: {Math.Round(2.567, 1)}");
        Console.WriteLine($"Techo de 2.3: {Math.Ceiling(2.3)}");
        Console.WriteLine($"Piso de 2.7: {Math.Floor(2.7)}");
        Console.WriteLine($"Truncar 2.9: {Math.Truncate(2.9)}");

        // --- Comparaciones ---
        Console.WriteLine($"Máximo entre 5 y 10: {Math.Max(5, 10)}");
        Console.WriteLine($"Mínimo entre 5 y 10: {Math.Min(5, 10)}");
        Console.WriteLine($"Clamp 12 entre 0 y 10: {Math.Clamp(12, 0, 10)}");

        // --- Logaritmos y exponenciales ---
        Console.WriteLine($"e elevado a 1: {Math.Exp(1)}");
        Console.WriteLine($"Logaritmo natural de 7.389: {Math.Log(7.389)}");
        Console.WriteLine($"Logaritmo base 10 de 1000: {Math.Log10(1000)}");

        // --- Trigonometría ---
        Console.WriteLine($"Seno de 45°: {Math.Sin(angulo)}");
        Console.WriteLine($"Coseno de 45°: {Math.Cos(angulo)}");
        Console.WriteLine($"Tangente de 45°: {Math.Tan(angulo)}");

        // --- Arcos ---
        Console.WriteLine($"Arco seno de 1: {Math.Asin(1)}");
        Console.WriteLine($"Arco coseno de 0: {Math.Acos(0)}");
        Console.WriteLine($"Arco tangente de 1: {Math.Atan(1)}");
        Console.WriteLine($"Arco tangente con Atan2(1,1): {Math.Atan2(1,1)}");

        // --- Hiperbólicas ---
        Console.WriteLine($"Seno hiperbólico de 1: {Math.Sinh(1)}");
        Console.WriteLine($"Coseno hiperbólico de 1: {Math.Cosh(1)}");
        Console.WriteLine($"Tangente hiperbólica de 1: {Math.Tanh(1)}");

        // --- Constantes ---
        Console.WriteLine($"Constante PI: {Math.PI}");
        Console.WriteLine($"Constante e: {Math.E}");

        // --- Residuo IEEE ---
        Console.WriteLine($"Residuo IEEE de 10/3: {Math.IEEERemainder(10, 3)}");

        Console.WriteLine("\n=== Fin de la demostración ===");
    }
}
```

---

#### 🔹 Qué hace este programa

1. Muestra **raíz cuadrada, cúbica y potencias**.
2. Aplica **valor absoluto** a números negativos.
3. Hace **redondeos**: `Round`, `Ceiling`, `Floor`, `Truncate`.
4. Compara valores con **Min, Max y Clamp**.
5. Usa **logaritmos y exponenciales**.
6. Trabaja con **trigonometría y arcos** (`Sin`, `Cos`, `Tan`, `Asin`, `Acos`, `Atan`, `Atan2`).
7. Incluye **funciones hiperbólicas**.
8. Muestra las **constantes matemáticas** `Math.PI` y `Math.E`.
9. Calcula el **residuo IEEE** con `Math.IEEERemainder`.

---

## 10.- Condicional `If`, `If-Else`, `Else If`, Ifs anidados

En C#, las estructuras condicionales permiten **tomar decisiones en el flujo de ejecución** basándose en expresiones booleanas (`true` o `false`). La más básica es el `if`.

---

### 10.1.- `if` simple

La forma más sencilla de usar un `if`:

```csharp
int edad = 18;

if (edad >= 18)
{
    Console.WriteLine("Eres mayor de edad.");
}
```

**Explicación:**

- La condición `edad >= 18` se evalúa a `true` o `false`.
- Si es `true`, se ejecuta el bloque de código dentro de `{}`.
- Si es `false`, se ignora.

**Tip:** En C#, **las llaves `{}` son opcionales si el bloque contiene solo una línea**:

```csharp
if (edad >= 18)
    Console.WriteLine("Eres mayor de edad.");
```

---

### 10.2.- `if-else`

Permite ejecutar un bloque alternativo si la condición es falsa:

```csharp
if (edad >= 18)
{
    Console.WriteLine("Mayor de edad.");
}
else
{
    Console.WriteLine("Menor de edad.");
}
```

**Tip:** También se puede usar sin llaves para un solo comando:

```csharp
if (edad >= 18)
    Console.WriteLine("Mayor de edad.");
else
    Console.WriteLine("Menor de edad.");
```

---

### 10.3.- `else if` (múltiples condiciones)

Cuando hay varias condiciones a evaluar:

```csharp
int nota = 85;

if (nota >= 90)
    Console.WriteLine("Excelente");
else if (nota >= 70)
    Console.WriteLine("Bueno");
else if (nota >= 50)
    Console.WriteLine("Suficiente");
else
    Console.WriteLine("Insuficiente");
```

**Tip:** Siempre termina con un `else` opcional para cubrir todos los casos.

---

### 10.4.- Ifs anidados

Puedes colocar un `if` dentro de otro `if`:

```csharp
int edad = 20;
bool licencia = true;

if (edad >= 18)
{
    if (licencia)
        Console.WriteLine("Puedes conducir.");
    else
        Console.WriteLine("Necesitas licencia.");
}
else
{
    Console.WriteLine("Eres menor de edad.");
}
```

**Tip de optimización:** Evita anidamientos profundos usando operadores lógicos combinados (`&&`, `||`) cuando sea posible:

```csharp
if (edad >= 18 && licencia)
    Console.WriteLine("Puedes conducir.");
else if (edad >= 18 && !licencia)
    Console.WriteLine("Necesitas licencia.");
else
    Console.WriteLine("Eres menor de edad.");
```

---

### 10.5.- Expresiones lógicas en `if`

Se pueden combinar condiciones con **AND (`&&`)**, **OR (`||`)**, y **NOT (`!`)**:

```csharp
int edad = 22;
bool tieneEntrada = false;

if (edad >= 18 && tieneEntrada)
    Console.WriteLine("Puedes entrar al concierto.");
else
    Console.WriteLine("No puedes entrar.");
```

**Tip:** Evita duplicar condiciones repetitivas combinando expresiones lógicas.

---

### 10.6.- `if` sin paréntesis (solo en C# 9 con expresiones lambda o patrones)

En C# clásico, **los paréntesis son obligatorios**.
Sin embargo, con **pattern matching** puedes simplificar la condición:

```csharp
object obj = 10;

if (obj is int n && n > 5)
    Console.WriteLine($"Número mayor que 5: {n}");
```

**Explicación:**

- `obj is int n` verifica el tipo y lo asigna a `n`.
- Se combina con `&& n > 5` en la misma condición.

---

### 10.7.- Operador ternario (`? :`) como alternativa a `if-else`

```csharp
int edad = 18;
string mensaje = (edad >= 18) ? "Mayor de edad" : "Menor de edad";
Console.WriteLine(mensaje);
```

**Tip:** Útil para expresiones cortas y asignaciones directas.

---

### 10.8.- Optimización de `if` en C #

1. **Evitar anidamientos profundos:** combina condiciones o usa `return` temprano.
2. **Usar `switch` cuando hay muchas condiciones sobre un mismo valor**.
3. **Usar operadores lógicos cortocircuito (`&&`, `||`)** para evaluar lo mínimo necesario.
4. **Pattern matching** para tipos y valores combinados, evita múltiples `if`.

```csharp
object obj = 10;

if (obj is int n && n > 0)
    Console.WriteLine("Número positivo");
else
    Console.WriteLine("No es un número positivo");
```

---

### 10.9.- Resumen de variantes de `if`

| Tipo de if                | Ejemplo corto                           | Uso recomendado                           |
| ------------------------- | --------------------------------------- | ----------------------------------------- |
| `if` simple               | `if (x>0) ...`                          | Decisión única                            |
| `if-else`                 | `if(x>0) ... else ...`                  | Decisión binaria                          |
| `if-else if-else`         | `if(x>0) ... else if(x<0) ... else ...` | Múltiples condiciones                     |
| If anidado                | `if(...) { if(...) { ... } }`           | Cuando condiciones dependen unas de otras |
| Pattern matching (`is`)   | `if(obj is int n && n>0)`               | Validación de tipo y valor                |
| Operador ternario (`? :`) | `string msg = (x>0)? "Pos" : "Neg"`     | Expresiones cortas                        |

---

### 10.10.- Operador ternario (`?:`)

El **operador ternario** es una forma compacta de escribir un `if-else` simple.

**Sintaxis básica:**

```csharp
condición ? valor_si_verdadero : valor_si_falso;
```

**Ejemplo 1: Asignación de variable**

```csharp
int edad = 20;
string mensaje = (edad >= 18) ? "Mayor de edad" : "Menor de edad";
Console.WriteLine(mensaje); // "Mayor de edad"
```

**Explicación paso a paso:**

1. `(edad >= 18)` → Evaluamos la condición, retorna `true` o `false`.
2. `? "Mayor de edad"` → Si es `true`, se asigna este valor.
3. `: "Menor de edad"` → Si es `false`, se asigna este valor.
4. Se puede asignar directamente a una variable o usarlo dentro de una expresión.

---

**Ejemplo 2: En llamadas a métodos**

```csharp
int numero = -5;
Console.WriteLine(numero >= 0 ? "Positivo" : "Negativo"); // "Negativo"
```

**Tip:**

- Evita usar ternarios muy largos, ya que disminuyen la legibilidad.
- Útil para **asignaciones rápidas**, **retornos de funciones** y **expresiones en línea**.

---

**Ejemplo 3: Ternario anidado**

```csharp
int nota = 85;
string resultado = (nota >= 90) ? "Excelente" :
                   (nota >= 70) ? "Bueno" :
                   (nota >= 50) ? "Suficiente" : "Insuficiente";

Console.WriteLine(resultado); // "Bueno"
```

**Tip:**

- Los ternarios anidados son válidos, pero **pueden volverse difíciles de leer**, por lo que se recomienda **siempre alinear y sangrar correctamente**.

---

### 10.11.- Pattern Matching (`is` y `switch`)

El **pattern matching** permite evaluar **tipo y/o valor** de una variable en una sola expresión, evitando múltiples `if` y castings innecesarios.

#### 10.11.1.- `is` con pattern matching

**Sintaxis básica:**

```csharp
if (variable is Tipo nombre && condición)
{
    // Código si coincide
}
```

**Ejemplo 1: Validar tipo y valor**

```csharp
object obj = 42;

if (obj is int n && n > 20)
{
    Console.WriteLine($"Número entero mayor que 20: {n}");
}
```

**Explicación:**

1. `obj is int n` → Verifica que `obj` es de tipo `int` y lo asigna a `n`.
2. `&& n > 20` → Evalúa una condición adicional sobre `n`.
3. Bloque se ejecuta solo si ambas condiciones son `true`.

---

**Ejemplo 2: Uso con `else`**

```csharp
object valor = "Hola";

if (valor is int numero)
    Console.WriteLine($"Número: {numero}");
else
    Console.WriteLine("No es un número.");
```

- Evita hacer `int numero = (int)valor;` que lanzaría excepción si el tipo no coincide.

---

#### 10.11.2.- Pattern Matching con `switch`

Desde C# 8+, se puede usar **switch expressions** para condicionales compactos basados en tipos y valores:

```csharp
object obj = 10;

string tipo = obj switch
{
    int n when n > 0 => "Entero positivo",
    int n when n < 0 => "Entero negativo",
    string s => $"Cadena de texto: {s}",
    _ => "Otro tipo"
};

Console.WriteLine(tipo); // "Entero positivo"
```

**Explicación:**

1. `int n when n > 0` → Coincide si `obj` es `int` y mayor que 0.
2. `string s` → Coincide si `obj` es cadena.
3. `_` → Catch-all, cualquier otro caso.
4. Permite **evitar múltiples `if-else` anidados**, manteniendo código legible y seguro.

---

#### 🔹10.11.3.- Ventajas del pattern matching

- Combina **validación de tipo** y **condición en un solo paso**.

- Evita **castings peligrosos** y errores en tiempo de ejecución.
- Funciona con **if**, **switch** y **expressions**.
- Mejora **legibilidad** y **mantenibilidad** del código.

---

## 11.- Switch en C #

El **`switch`** es una estructura de control que permite seleccionar entre múltiples opciones basadas en el valor de una variable. Es una alternativa más **limpia y legible** que usar muchos `if-else if-else`.

---

### 11.1.- Sintaxis básica del switch

```csharp
int dia = 3;

switch (dia)
{
    case 1:
        Console.WriteLine("Lunes");
        break;
    case 2:
        Console.WriteLine("Martes");
        break;
    case 3:
        Console.WriteLine("Miércoles");
        break;
    default:
        Console.WriteLine("Otro día");
        break;
}
```

**Explicación:**

1. `switch (dia)` → Se evalúa el valor de `dia`.
2. Cada `case` compara con un valor literal.
3. `break` → Evita que se ejecute el siguiente `case` (“fall-through”).
4. `default` → Bloque opcional que se ejecuta si ningún `case` coincide.

---

### 11.2.- Switch sin `break` (fall-through explícito)

En C#, **no se permite “caída libre”** como en C/C++: cada `case` debe terminar con `break`, `return` o `goto`.

```csharp
int numero = 2;

switch (numero)
{
    case 1:
    case 2:
        Console.WriteLine("Número 1 o 2");
        break;
    default:
        Console.WriteLine("Otro número");
        break;
}
```

- Aquí **case 1 y case 2** comparten el mismo bloque de código.
- Útil para agrupar valores.

---

### 11.3.- Switch con múltiples tipos de valores

```csharp
string letra = "a";

switch (letra)
{
    case "a":
    case "A":
        Console.WriteLine("Vocal A");
        break;
    case "e":
    case "E":
        Console.WriteLine("Vocal E");
        break;
    default:
        Console.WriteLine("Otra letra");
        break;
}
```

- Puede usarse con **`int`**, **`string`**, **`char`**, **enum**, etc.

---

### 11.4.- Switch con expresiones (C# 8+)

Desde C# 8, se puede usar **`switch expressions`**, que son más compactas:

```csharp
int nota = 85;

string resultado = nota switch
{
    >= 90 => "Excelente",
    >= 70 => "Bueno",
    >= 50 => "Suficiente",
    _ => "Insuficiente"
};

Console.WriteLine(resultado); // "Bueno"
```

**Explicación:**

1. Cada línea representa un **patrón** (`>=90`) y el valor a devolver (`"Excelente"`).
2. `_` → patrón por defecto, equivalente a `default`.
3. Retorna un valor directamente, ideal para asignaciones.

---

### 11.5.- Switch con patrones (Pattern Matching)

C# permite **combinar switch con tipos y condiciones**:

```csharp
object obj = 10;

string tipo = obj switch
{
    int n when n > 0 => "Entero positivo",
    int n when n < 0 => "Entero negativo",
    string s => $"Cadena: {s}",
    _ => "Otro tipo"
};

Console.WriteLine(tipo); // "Entero positivo"
```

- Se puede evaluar **tipo** y **condición** en la misma expresión.
- Evita múltiples `if-else` anidados y castings inseguros.

---

### 11.6.- Switch con tuplas

C# permite usar **tuplas** para evaluar múltiples variables al mismo tiempo:

```csharp
(int x, int y) punto = (1, -1);

string cuadrante = punto switch
{
    ( > 0, > 0) => "Primer cuadrante",
    ( < 0, > 0) => "Segundo cuadrante",
    ( < 0, < 0) => "Tercer cuadrante",
    ( > 0, < 0) => "Cuarto cuadrante",
    _ => "Origen o eje"
};

Console.WriteLine(cuadrante); // "Cuarto cuadrante"
```

- Muy útil para **combinaciones de valores** y geometría, entre otros casos.

---

### 11.7.- Switch con enums

```csharp
enum Dias { Lunes, Martes, Miercoles, Jueves, Viernes }

Dias dia = Dias.Miercoles;

switch (dia)
{
    case Dias.Lunes:
        Console.WriteLine("Inicio de semana");
        break;
    case Dias.Viernes:
        Console.WriteLine("Fin de semana");
        break;
    default:
        Console.WriteLine("Día intermedio");
        break;
}
```

- Los **enums** hacen los switch más legibles y seguros.

---

### 11.8.- Optimización de switches

1. **Usar switch expressions** en lugar de switch tradicional cuando se devuelve un valor.
2. **Agrupar cases** que ejecutan lo mismo para evitar código repetido.
3. **Usar pattern matching** para validar tipos y rangos en un solo paso.
4. Evitar `switch` excesivamente largo, considerar **diccionarios** para mapas clave → valor.

---

### 11.9.- Consejos y buenas prácticas

- Siempre incluir un **`default`** (o `_` en expresiones) para casos inesperados.
- Evita lógica compleja dentro de los `case`; mejor llamar a **métodos separados**.
- Prefiere **switch expressions** para retornos simples, asignaciones y legibilidad.
- Usa **switch con tuplas o patrones** para combinar varias condiciones sin anidar `if`.

---

### 11.10.- Resumen de variantes de switch

| Tipo de switch              | Ejemplo corto                          | Cuándo usar                 |
| --------------------------- | -------------------------------------- | --------------------------- |
| Switch clásico con `case`   | `switch(x){ case 1: ... break; }`      | Múltiples valores discretos |
| Switch agrupado             | `case 1: case 2: ... break;`           | Casos que comparten acción  |
| Switch expression (C# 8+)   | `var res = x switch { ... }`           | Retorno de valores simples  |
| Switch con pattern matching | `obj switch { int n when n>0 => ... }` | Tipos + condiciones         |
| Switch con tuplas           | `(x,y) switch { ... }`                 | Evaluar múltiples variables |
| Switch con enums            | `switch(dia)`                          | Legible y seguro            |

---

## 12.-🧩 Diferencia entre *Tupla* y *Enum* en C #

Primero que nada:
👉 Ambos existen en C#, pero **sirven para cosas totalmente distintas**.

---

### 🧱 1. ENUM — *Tipo de dato definido por el programador*

Un **enum (enumeración)** es un **tipo de dato especial** que te permite **nombrar valores numéricos constantes**.

#### Ejemplo de ENUM

```csharp
enum Dias
{
    Lunes,     // 0
    Martes,    // 1
    Miercoles, // 2
    Jueves,    // 3
    Viernes    // 4
}
```

Esto crea un **nuevo tipo de dato** llamado `Dias`.
Puedes usarlo así:

```csharp
Dias hoy = Dias.Miercoles;

if (hoy == Dias.Miercoles)
    Console.WriteLine("¡Mitad de semana!");
```

#### ✳️ Características de ENUM

| Concepto           | Valor                                                    |
| ------------------ | -------------------------------------------------------- |
| **Qué es**         | Tipo de dato definido por el usuario                     |
| **Internamente**   | Representa valores numéricos enteros (por defecto `int`) |
| **Uso típico**     | Estados, días, modos, tipos (categorías discretas)       |
| **Ventajas**       | Código más legible, evita números mágicos                |
| **Ejemplo de uso** | Estados de un juego, tipos de usuario, días de la semana |

📘 En resumen:

> Un **enum** es una forma de crear un tipo de dato con valores *predefinidos* y *nombrados*.

---

### 🧮 2. TUPLA — *Estructura de datos que agrupa valores distintos*

Una **tupla** no es un tipo de dato predefinido, sino una **estructura** que permite **empaquetar varios valores (de distintos tipos)** en una sola unidad.

#### Ejemplo de tupla

```csharp
var persona = ("Lechu", 28, true);
Console.WriteLine($"Nombre: {persona.Item1}, Edad: {persona.Item2}, Activo: {persona.Item3}");
```

O más limpio con nombres:

```csharp
var persona = (Nombre: "Lechu", Edad: 28, Activo: true);
Console.WriteLine($"Hola {persona.Nombre}, edad: {persona.Edad}");
```

#### ✳️ Características de Tupla

| Concepto           | Valor                                                                                      |
| ------------------ | ------------------------------------------------------------------------------------------ |
| **Qué es**         | Estructura de datos que agrupa múltiples valores                                           |
| **Internamente**   | Un objeto de tipo `ValueTuple<T1, T2, T3, ...>`                                            |
| **Uso típico**     | Retornar varios valores de una función, agrupar datos temporales                           |
| **Ventajas**       | No necesitas crear una clase solo para agrupar datos                                       |
| **Ejemplo de uso** | Retornar `(x, y)` de una función de coordenadas, o `(resultado, mensaje)` de una operación |

📘 En resumen:

> Una **tupla** es una “mini estructura de datos” que contiene múltiples valores (de tipos distintos o iguales) sin necesidad de una clase.

---

### ⚖️ Comparación directa

| Característica                 | **Enum**                                      | **Tupla**                                            |
| ------------------------------ | --------------------------------------------- | ---------------------------------------------------- |
| Tipo de entidad                | Tipo de dato definido por el usuario          | Estructura de datos                                  |
| Propósito                      | Representar un conjunto de valores constantes | Agrupar varios valores en una sola variable          |
| Tipos que puede contener       | Solo números enteros (normalmente)            | Cualquier tipo (`int`, `string`, `bool`, etc.)       |
| Mutabilidad                    | Inmutable (no cambia su definición)           | Mutable (puedes reasignar valores)                   |
| Ejemplo                        | `enum Estado { Activo, Inactivo }`            | `var punto = (x: 10, y: 20)`                         |
| Uso común                      | Estados, categorías, banderas                 | Retornar múltiples valores, pasar conjuntos de datos |
| Equivalente en otros lenguajes | Enum de Java, Enum de C++                     | Tuple de Python, struct ligera                       |

 🧠 En pocas palabras

| Si necesitas...                                                     | Usa...    |
| ------------------------------------------------------------------- | --------- |
| Representar un conjunto fijo de valores (como días, estados, roles) | **Enum**  |
| Empaquetar varios datos (como nombre, edad, estado)                 | **Tupla** |

 💡 Tip ingenieril

- Usa **enum** para **clasificar** cosas (e.g. tipos de enemigo, modos de juego, niveles de dificultad).
- Usa **tuplas** para **transportar datos rápidamente**, especialmente como **retorno de funciones**.

## 13.- Ciclo `for` en C #

### 13.0 Introducción

El ciclo **`for`** se utiliza cuando **sabes cuántas veces quieres repetir una instrucción o bloque de código**.
Es ideal para recorrer arreglos, listas, ejecutar operaciones repetitivas o iterar con condiciones controladas.

---

### 🔹 13.1 Estructura básica del `for`

```csharp
for (inicialización; condición; actualización)
{
    // Bloque de código a ejecutar
}
```

- 🧠 Explicación

1. **Inicialización:** se ejecuta una sola vez antes de comenzar el ciclo.
2. **Condición:** se evalúa antes de cada iteración. Si es `true`, el ciclo continúa; si es `false`, se detiene.
3. **Actualización:** se ejecuta al final de cada iteración.

---

#### 🧩 Ejemplo simple

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine($"Iteración número: {i}");
}
```

📘 **Salida:**

```yaml
Iteración número: 0
Iteración número: 1
Iteración número: 2
Iteración número: 3
Iteración número: 4
```

---

### 🔹 13.2 Partes del `for` explicadas

| Parte              | Qué hace                             | Ejemplo     |
| ------------------ | ------------------------------------ | ----------- |
| **Inicialización** | Crea y define la variable de control | `int i = 0` |
| **Condición**      | Evalúa si continúa el ciclo          | `i < 5`     |
| **Actualización**  | Modifica la variable                 | `i++`       |

> 💡 Puedes usar cualquier operador en la actualización: `i++`, `i--`, `i += 2`, `i *= 2`, etc.

---

### 🔹 13.3 Tipos y variaciones del `for`

#### 1️⃣ For clásico (más usado)

```csharp
for (int i = 0; i < 10; i++)
    Console.WriteLine(i);
```

#### 2️⃣ For decreciente

```csharp
for (int i = 10; i >= 0; i--)
    Console.WriteLine(i);
```

#### 3️⃣ For con paso personalizado

```csharp
for (int i = 0; i <= 20; i += 5)
    Console.WriteLine(i);
```

#### 4️⃣ For sin cuerpo

Cuando el cuerpo del ciclo es una sola instrucción:

```csharp
for (int i = 0; i < 5; Console.WriteLine(i++));
```

#### 5️⃣ For infinito (cuidado ⚠️)

```csharp
for (;;)
{
    Console.WriteLine("Loop infinito...");
    break; // sin esto, nunca termina
}
```

---

### 🔹 13.4 Variantes más modernas

#### 🔸 13.4.1 For con múltiples variables

Puedes inicializar y actualizar más de una variable:

```csharp
for (int i = 0, j = 10; i < j; i++, j--)
{
    Console.WriteLine($"i = {i}, j = {j}");
}
```

#### 🔸 13.4.2 For con listas o colecciones (cuando no quieres usar foreach)

```csharp
string[] nombres = { "Lechu", "Dev", "Skater" };

for (int i = 0; i < nombres.Length; i++)
{
    Console.WriteLine($"Nombre {i}: {nombres[i]}");
}
```

---

### 🔹 13.5 Optimización del `for`

#### 🧠 1️⃣ Evita recalcular longitudes en cada iteración

❌ Incorrecto:

```csharp
for (int i = 0; i < lista.Count; i++)
```

✅ Correcto:

```csharp
int n = lista.Count;
for (int i = 0; i < n; i++)
```

#### 🧠 2️⃣ Prefiere `foreach` si solo necesitas recorrer una colección

Menos propenso a errores y más legible:

```csharp
foreach (var item in lista)
    Console.WriteLine(item);
```

#### 🧠 3️⃣ Evita operaciones costosas dentro del ciclo

Calcula valores una sola vez antes del `for` si no cambian.

#### 🧠 4️⃣ Usa paralelismo si el ciclo es muy pesado

Para tareas grandes puedes usar:

```csharp
Parallel.For(0, 100, i => {
    // Ejecución paralela
});
```

---

### 🔹 13.6 Combinando `for` con condiciones

```csharp
for (int i = 0; i < 10; i++)
{
    if (i % 2 == 0)
        Console.WriteLine($"{i} es par");
    else
        Console.WriteLine($"{i} es impar");
}
```

---

### 🔹 13.7 Uso de `break` y `continue`

#### 🔸 `break`

Sale completamente del ciclo:

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
        break;
    Console.WriteLine(i);
}
```

#### 🔸 `continue`

Salta a la siguiente iteración:

```csharp
for (int i = 0; i < 10; i++)
{
    if (i % 2 != 0)
        continue;
    Console.WriteLine(i); // Solo imprime los pares
}
```

---

### 🔹 13.8 For anidado

Permite ciclos dentro de otros ciclos:

```csharp
for (int i = 1; i <= 3; i++)
{
    for (int j = 1; j <= 2; j++)
    {
        Console.WriteLine($"i = {i}, j = {j}");
    }
}
```

📘 **Salida:**

```yaml
i = 1, j = 1
i = 1, j = 2
i = 2, j = 1
i = 2, j = 2
i = 3, j = 1
i = 3, j = 2
```

---

### 🔹 13.9 Ejemplo práctico — Tabla de multiplicar

```csharp
Console.Write("Ingresa un número: ");
int numero = int.Parse(Console.ReadLine());

for (int i = 1; i <= 10; i++)
{
    Console.WriteLine($"{numero} x {i} = {numero * i}");
}
```

---

### 🔹 13.10 Buenas prácticas para usar `for`

✅ Usa nombres descriptivos en variables (`i`, `j`, `index`, etc.)
✅ No hagas ciclos innecesarios (rompe con `break` si ya obtuviste lo que buscas)
✅ Evita modificar la colección que estás recorriendo dentro del `for`
✅ Prefiere `foreach` si no necesitas el índice
✅ Usa `Parallel.For` solo si las iteraciones no dependen entre sí

---

### 🧩 13.11 Mini resumen final

| Tipo de `for`       | Descripción                  | Ejemplo                                     |
| ------------------- | ---------------------------- | ------------------------------------------- |
| Clásico             | Ciclo normal con contador    | `for (int i=0;i<10;i++)`                    |
| Decreciente         | Itera hacia atrás            | `for (int i=10;i>=0;i--)`                   |
| Sin cuerpo          | Todo dentro del paréntesis   | `for (int i=0;i<5;Console.WriteLine(i++));` |
| Infinito            | No tiene condición           | `for(;;){}`                                 |
| Múltiples variables | Controla más de una a la vez | `for(int i=0,j=10;i<j;i++,j--)`             |

---

## 14.- Ciclo `foreach`

El ciclo **`foreach`** en C# es una forma simplificada y **segura** de recorrer colecciones, arreglos, listas o cualquier tipo de dato que implemente la interfaz `IEnumerable` o `IEnumerable<T>`.
Es decir: **sirve para iterar sobre elementos sin preocuparte por índices ni límites**.

---

### 🧱 Declaración básica

```csharp
foreach (tipo elemento in coleccion)
{
    // Código a ejecutar en cada iteración
}
```

Ejemplo:

```csharp
string[] frutas = { "Manzana", "Banana", "Pera" };

foreach (string fruta in frutas)
{
    Console.WriteLine(fruta);
}
```

🔹 El ciclo recorre **automáticamente** todos los elementos de la colección.
🔹 `fruta` toma el valor de cada elemento en cada iteración.
🔹 No necesitas manejar contadores ni índices (como en `for`).

---

### 🧩 Cómo funciona internamente

Detrás del telón, `foreach` usa un **iterador** que llama internamente a los métodos:

- `GetEnumerator()` → obtiene el enumerador.
- `MoveNext()` → avanza al siguiente elemento.
- `Current` → obtiene el elemento actual.

Así que esto:

```csharp
foreach (var item in lista)
{
    Console.WriteLine(item);
}
```

equivale a esto:

```csharp
var enumerador = lista.GetEnumerator();

while (enumerador.MoveNext())
{
    var item = enumerador.Current;
    Console.WriteLine(item);
}
```

⚙️ Es decir, `foreach` es una forma elegante de escribir el patrón del enumerador.

---

### 🧮 Tipos de colecciones compatibles

`foreach` funciona con cualquier tipo que implemente:

- `IEnumerable`
- `IEnumerable<T>`
- `IEnumerator`
- `IEnumerator<T>`

Ejemplos comunes:

```csharp
int[] numeros = { 1, 2, 3, 4 };
List<string> nombres = new List<string>() { "Ana", "Luis", "Carlos" };
Dictionary<int, string> diccionario = new Dictionary<int, string>()
{
    {1, "Uno"},
    {2, "Dos"}
};
```

---

### 📚 Ejemplo con diccionarios

```csharp
var precios = new Dictionary<string, int>()
{
    {"Manzana", 10},
    {"Banana", 5},
    {"Pera", 7}
};

foreach (var par in precios)
{
    Console.WriteLine($"{par.Key}: ${par.Value}");
}
```

También puedes iterar solo las claves o los valores:

```csharp
foreach (var clave in precios.Keys)
    Console.WriteLine(clave);

foreach (var valor in precios.Values)
    Console.WriteLine(valor);
```

---

### 🧠 Inmutabilidad del elemento

En un `foreach`, **el valor del elemento es de solo lectura**.
No puedes modificar directamente el elemento dentro del ciclo.

❌ Esto **no funciona**:

```csharp
foreach (int n in numeros)
{
    n *= 2; // Error: n es de solo lectura
}
```

✅ Para modificar los elementos, usa un `for` clásico:

```csharp
for (int i = 0; i < numeros.Length; i++)
{
    numeros[i] *= 2;
}
```

---

### ⚡ Optimización y buenas prácticas

1. **Evita usar `foreach` en colecciones que cambian durante la iteración.**

   - Modificar la colección lanza `InvalidOperationException`.

2. **Prefiere `foreach` sobre `for` cuando solo necesites leer los valores.**

   - Es más limpio y menos propenso a errores de índice.

3. **Usa `for` si necesitas conocer el índice.**

   - En `foreach`, el índice no está disponible por defecto (aunque puedes generarlo manualmente).

4. **Usa LINQ o métodos funcionales si quieres filtrar o transformar colecciones.**

Ejemplo:

```csharp
foreach (var numero in numeros.Where(n => n > 5))
{
    Console.WriteLine(numero);
}
```

---

### 🧩 `foreach` con índice (truco)

Aunque `foreach` no tiene índice directamente, puedes usar `Select` de LINQ:

```csharp
var frutas = new[] { "Manzana", "Pera", "Uva" };

foreach (var (fruta, i) in frutas.Select((valor, indice) => (valor, indice)))
{
    Console.WriteLine($"Fruta {i}: {fruta}");
}
```

---

### 🔄 Variantes y equivalentes

| Variante           | Descripción                                        | Ejemplo                             |
| ------------------ | -------------------------------------------------- | ----------------------------------- |
| `foreach` normal   | Itera sobre colección                              | `foreach (var x in lista)`          |
| `Parallel.ForEach` | Ejecuta iteraciones en paralelo (multi-hilo)       | `Parallel.ForEach(lista, x => ...)` |
| `await foreach`    | Itera sobre flujos asíncronos (`IAsyncEnumerable`) | `await foreach (var item in flujo)` |

---

### 🚀 Ejemplo de `await foreach` (C# 8+)

```csharp
static async IAsyncEnumerable<int> GenerarNumerosAsync()
{
    for (int i = 1; i <= 3; i++)
    {
        await Task.Delay(500);
        yield return i;
    }
}

static async Task Main()
{
    await foreach (var numero in GenerarNumerosAsync())
    {
        Console.WriteLine(numero);
    }
}
```

👉 Permite **procesar datos en streaming** (muy útil para lecturas asíncronas o APIs).

---

### 🧭 Resumen

| Concepto                   | `for`              | `foreach`           |
| -------------------------- | ------------------ | ------------------- |
| Control de índice          | ✅                  | ❌                   |
| Lectura de datos           | ✅                  | ✅                   |
| Modificación de elementos  | ✅                  | ❌                   |
| Sintaxis más limpia        | ❌                  | ✅                   |
| Compatible con colecciones | ✅                  | ✅                   |
| Riesgo de error de índice  | Alto               | Nulo                |
| Asincronía                 | Con `Parallel.For` | Con `await foreach` |

---
🧩 **Conclusión**

El ciclo `foreach` es **seguro, expresivo y fácil de leer**, ideal para recorrer colecciones sin preocuparte por límites ni errores de índice.
Usa `for` si necesitas **modificar elementos o controlar el índice**; usa `foreach` si solo **quieres recorrer o procesar datos**.

## 15.- Ciclos `while` y `do while`

Estos dos ciclos permiten ejecutar código **mientras** una condición sea verdadera.
La diferencia está en **cuándo se evalúa la condición**:

- `while` la evalúa **antes** de entrar al bloque.
- `do while` la evalúa **después**, garantizando al menos una ejecución.

---

### 🧱 Ciclo `while` – Estructura básica

```csharp
while (condición)
{
    // Código que se ejecuta mientras la condición sea verdadera
}
```

Ejemplo:

```csharp
int contador = 0;

while (contador < 5)
{
    Console.WriteLine($"Iteración {contador}");
    contador++;
}
```

📊 Este ciclo imprimirá del 0 al 4.
Si la condición no se cumple al inicio, **el bloque no se ejecuta nunca**.

---

### 🧩 Ciclo `do while` – Estructura básica

```csharp
do
{
    // Código que se ejecuta al menos una vez
} while (condición);
```

Ejemplo:

```csharp
int numero = 5;

do
{
    Console.WriteLine($"Número actual: {numero}");
    numero--;
} while (numero > 0);
```

📌 A diferencia del `while`, **si la condición es falsa desde el inicio**, este ciclo **se ejecuta una vez de todas formas**.

---

### 🔄 Comparación rápida

| Característica                   | `while`       | `do while`      |
| -------------------------------- | ------------- | --------------- |
| Evalúa antes de ejecutar         | ✅             | ❌               |
| Evalúa después de ejecutar       | ❌             | ✅               |
| Se puede ejecutar cero veces     | ✅             | ❌               |
| Siempre ejecuta al menos una vez | ❌             | ✅               |
| Uso típico                       | Validar antes | Validar después |

---

### ⚙️ Ejemplo práctico: menú interactivo

```csharp
string opcion;

do
{
    Console.WriteLine("1. Saludar");
    Console.WriteLine("2. Despedirse");
    Console.WriteLine("3. Salir");
    Console.Write("Elige una opción: ");
    opcion = Console.ReadLine();

    switch (opcion)
    {
        case "1":
            Console.WriteLine("¡Hola!");
            break;
        case "2":
            Console.WriteLine("Adiós!");
            break;
    }

} while (opcion != "3");
```

💡 Aquí `do while` es ideal porque **queremos mostrar el menú al menos una vez**.

---

### ⚡ Consejos y buenas prácticas

1. **Evita bucles infinitos no controlados**

   ```csharp
   while(true) { ... } // peligroso si no hay break
   ```

   Si los usas, asegúrate de incluir una **condición de salida** con `break`:

   ```csharp
   while(true)
   {
       string entrada = Console.ReadLine();
       if (entrada == "salir") break;
   }
   ```

2. **Cuida las variables de control**
   Siempre asegúrate de **modificar la variable** que afecta la condición, o nunca saldrás del bucle.

3. **Usa `while` cuando no sabes cuántas iteraciones habrá**
   Ejemplo: leer datos hasta que el usuario introduzca “fin”.

4. **Usa `do while` cuando quieras ejecutar algo al menos una vez**, como un menú o validación de entrada.

---

### 🧮 Optimización de ciclos `while`

- Si trabajas con colecciones o índices fijos, **prefiere `for` o `foreach`** (más claros y seguros).
- Si repites operaciones costosas dentro del ciclo, **extrae cálculos fuera** del `while`.

❌ Ineficiente:

```csharp
while (lista.Count > 0)
{
    lista.RemoveAt(0);
}
```

✅ Mejor:

```csharp
int count = lista.Count;
for (int i = 0; i < count; i++)
{
    lista.RemoveAt(0);
}
```

---

### 💡 Uso con `break` y `continue`

```csharp
int i = 0;
while (i < 10)
{
    i++;

    if (i == 3)
        continue; // salta el resto del bloque

    if (i == 8)
        break; // rompe el ciclo

    Console.WriteLine(i);
}
```

Resultado:
Imprime del 1 al 10, **saltando el 3 y deteniéndose al llegar al 8**.

---

### 🧠 `while` infinito controlado (bucles de servicio)

A veces se usan intencionalmente para procesos que deben correr siempre:

```csharp
while (true)
{
    ProcesarEventos();
    Thread.Sleep(1000);
}
```

⚠️ Estos ciclos deben tener **algún mecanismo de salida o pausa**, como una bandera booleana o una señal externa.

---

### 🧩 Resumen general

| Tipo de ciclo | Cuándo se evalúa | Puede no ejecutarse | Ideal para...                          |
| ------------- | ---------------- | ------------------- | -------------------------------------- |
| `for`         | Antes            | ✅                   | Iteraciones contadas                   |
| `foreach`     | Automático       | ✅                   | Recorrer colecciones                   |
| `while`       | Antes            | ✅                   | Condiciones dinámicas                  |
| `do while`    | Después          | ❌                   | Ejecución garantizada al menos una vez |

---

### 🚀 Conclusión

Los ciclos `while` y `do while` son poderosos para controlar **flujo condicional repetitivo**.

- Usa `while` cuando **quieras verificar antes de ejecutar**.
- Usa `do while` cuando **necesites ejecutar al menos una vez antes de verificar**.
  Ambos son esenciales cuando la cantidad de iteraciones **no está definida de antemano**.

---

¿Deseas que sigamos con el **tema 16: Ciclo `break`, `continue` y `goto`** (control de flujo dentro de bucles)?
Puedo hacerlo con ejemplos, advertencias y optimizaciones.

## 16.- Control de Flujo: `break`, `continue` y `goto`

Los ciclos (`for`, `foreach`, `while`, `do while`) ejecutan bloques repetitivos de código, pero muchas veces necesitamos **romper, saltar o redirigir** el flujo según condiciones específicas.
Para eso existen estas tres palabras clave:

---

### 🧩 1️⃣ `break` — Rompe el ciclo actual

Sirve para **salir inmediatamente** del ciclo (o `switch`) en el que se encuentra.
No se ejecuta el resto del bloque ni se sigue iterando.

---

#### 🔹 Ejemplo básico

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
        break; // rompe el ciclo cuando i == 5

    Console.WriteLine(i);
}
```

🧠 Resultado:

```yaml
0
1
2
3
4
```

El ciclo se detiene al llegar al `break`.

---

#### 🔹 Uso en `while` y `foreach`

```csharp
int numero = 0;
while (true)
{
    numero++;
    if (numero == 3)
        break; // sale del ciclo infinito

    Console.WriteLine(numero);
}
```

---

#### ⚙️ Casos de uso comunes

- Finalizar un ciclo al cumplir una condición.
- Salir de un menú interactivo.
- Romper una búsqueda al encontrar un resultado.

---

### 🧩 2️⃣ `continue` — Salta a la siguiente iteración

Omite el resto del código dentro del bloque y **pasa directamente a la siguiente iteración** del ciclo.

---

#### 🔹 Ejemplo básico de `continue`

```csharp
for (int i = 0; i < 5; i++)
{
    if (i == 2)
        continue; // salta la iteración cuando i == 2

    Console.WriteLine(i);
}
```

🧠 Resultado:

```yaml
0
1
3
4
```

La iteración donde `i == 2` se salta por completo.

---

#### 🔹 Ejemplo práctico con `while`

```csharp
int i = 0;

while (i < 5)
{
    i++;
    if (i % 2 == 0)
        continue; // omite los pares

    Console.WriteLine(i);
}
```

🧮 Resultado:

```yaml
1
3
5
```

---

#### ⚙️ Usos típicos

- Saltar iteraciones que no cumplen un criterio.
- Evitar anidar demasiados `if` dentro de los bucles.
- Mejorar la legibilidad de condiciones complejas.

---

### 🧩 3️⃣ `goto` — Salto directo a una etiqueta

El temido (y mal comprendido) **`goto`** permite **saltar a una etiqueta específica del código**.
Su uso se considera **poco recomendado**, porque puede romper la estructura lógica del programa y volverlo difícil de mantener.

---

#### 🔹 Sintaxis básica

```csharp
goto etiqueta;

// ...
etiqueta:
Console.WriteLine("Salto completado.");
```

---

#### 🔹 Ejemplo práctico

```csharp
int i = 0;

while (true)
{
    if (i == 3)
        goto Salir; // salta al final del programa

    Console.WriteLine(i);
    i++;
}

Salir:
Console.WriteLine("Fin del ciclo.");
```

🧠 Resultado:

```yaml
0
1
2
Fin del ciclo.
```

---

#### ⚠️ Cuándo (y cuándo NO) usar `goto`

**✅ Casos válidos:**

- Para salir de varios ciclos anidados de una sola vez.
- En código muy bajo nivel o control de errores críticos (poco común en C# moderno).

**❌ Evítalo cuando:**

- Se puede resolver con `break`, `continue` o funciones separadas.
- Hace el código más difícil de leer.

---

#### 🔹 Ejemplo: romper varios bucles anidados

```csharp
for (int i = 0; i < 5; i++)
{
    for (int j = 0; j < 5; j++)
    {
        if (i == 2 && j == 3)
            goto Salir; // rompe ambos ciclos

        Console.WriteLine($"{i}, {j}");
    }
}

Salir:
Console.WriteLine("Ciclos terminados.");
```

🧠 Sin `goto`, tendrías que usar variables booleanas o funciones auxiliares.

---

### ⚡ Resumen general

| Palabra clave | Función                          | Rompe el ciclo | Salta iteración | Salta a otro punto |
| ------------- | -------------------------------- | -------------- | --------------- | ------------------ |
| `break`       | Sale del ciclo o `switch` actual | ✅              | ❌               | ❌                  |
| `continue`    | Salta a la siguiente iteración   | ❌              | ✅               | ❌                  |
| `goto`        | Salta a una etiqueta específica  | ✅              | ❌               | ✅                  |

---

### 🧠 Optimización y buenas prácticas

1. Usa `break` y `continue` para **claridad de flujo**, no para esconder mala lógica.
2. Evita `goto` salvo casos muy específicos.
3. Si un ciclo tiene muchas condiciones de salida, **replantea el diseño** (quizás divídelo en funciones).
4. Usa `return` si estás dentro de un método y deseas terminar **todo el proceso**, no solo el ciclo.

---

#### 💡 **Ejemplo avanzado: combinación de control**

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 3)
        continue; // salta el 3

    if (i == 8)
        break; // termina el ciclo

    Console.WriteLine(i);
}
```

🧮 Resultado:

```yaml
0
1
2
4
5
6
7
```

---

#### 🧩 **Conclusión**

- 🔸 **`break`** → Detén el ciclo actual.
- 🔸 **`continue`** → Salta la iteración actual.
- 🔸 **`goto`** → Salta a una etiqueta (usa con precaución).

Dominar estas palabras te da **control total sobre el flujo interno de tus bucles**, evitando redundancias y mejorando el rendimiento lógico de tu código.

## 🧮 17.- Matrices en C# (Arrays)

En C#, una **matriz (array)** es una **colección de elementos del mismo tipo** almacenados en posiciones contiguas de memoria.
Cada elemento se accede mediante un **índice**, que siempre empieza en **0**.

Las matrices son muy útiles para manejar listas, tablas, colecciones de datos numéricos o cadenas, y forman la base de estructuras más complejas como listas, colas, pilas y matrices multidimensionales.

---

### 🔹 17.1.- Declaración y creación de matrices

Hay varias formas de **declarar e inicializar** matrices en C#:

```csharp
// Declaración vacía (sin datos)
int[] numeros;

// Declaración e inicialización con tamaño
numeros = new int[5]; // Crea un array con 5 elementos (índices 0–4)

// Declaración e inicialización con valores
int[] edades = { 18, 22, 25, 30, 40 };
```

🧠 En el tercer caso, el compilador deduce el tamaño automáticamente (en este ejemplo, 5 elementos).

---

### 🔹 17.2.- Acceso y modificación de elementos

Cada elemento se accede con su **índice**:

```csharp
int[] edades = { 18, 22, 25, 30, 40 };

// Acceder a un elemento
Console.WriteLine(edades[2]); // Muestra 25

// Modificar un elemento
edades[2] = 26;
Console.WriteLine(edades[2]); // Muestra 26
```

⚠️ Si intentas acceder a un índice fuera del rango (`edades[10]`), obtendrás una **excepción `IndexOutOfRangeException`**.

---

### 🔹 17.3.- Recorrer matrices con `for` y `foreach`

**Con `for`:**

```csharp
int[] numeros = { 10, 20, 30, 40 };

for (int i = 0; i < numeros.Length; i++)
{
    Console.WriteLine($"Elemento {i}: {numeros[i]}");
}
```

**Con `foreach`:**

```csharp
foreach (int n in numeros)
{
    Console.WriteLine($"Valor: {n}");
}
```

🧩 `foreach` es más legible, pero `for` da más control sobre los índices.

---

### 🔹 17.4.- Matrices multidimensionales

C# soporta **matrices de más de una dimensión** (bidimensionales, tridimensionales, etc.).

#### Ejemplo de matriz bidimensional (como una tabla)

```csharp
int[,] matriz = new int[2, 3] { { 1, 2, 3 }, { 4, 5, 6 } };
```

Visualmente:

```Yaml
1  2  3
4  5  6
```

**Acceso:**

```csharp
Console.WriteLine(matriz[0, 1]); // 2
```

**Recorrido:**

```csharp
for (int fila = 0; fila < matriz.GetLength(0); fila++)
{
    for (int col = 0; col < matriz.GetLength(1); col++)
    {
        Console.Write($"{matriz[fila, col]} ");
    }
    Console.WriteLine();
}
```

---

### 🔹 17.5.- Matrices irregulares (Jagged Arrays)

Un **jagged array** es un array de arrays, donde cada subarray puede tener diferente tamaño.

```csharp
int[][] jagged = new int[3][];
jagged[0] = new int[] { 1, 2 };
jagged[1] = new int[] { 3, 4, 5 };
jagged[2] = new int[] { 6 };
```

**Recorrido:**

```csharp
for (int i = 0; i < jagged.Length; i++)
{
    for (int j = 0; j < jagged[i].Length; j++)
    {
        Console.Write($"{jagged[i][j]} ");
    }
    Console.WriteLine();
}
```

🧠 Ideal cuando cada fila tiene distinta cantidad de datos (por ejemplo, alumnos con diferente número de calificaciones).

---

### 🔹 17.6.- Métodos útiles de la clase `Array`

C# provee muchos métodos para manipular arrays fácilmente:

| Método                      | Descripción                                 |
| --------------------------- | ------------------------------------------- |
| `Array.Sort(array)`         | Ordena los elementos                        |
| `Array.Reverse(array)`      | Invierte el orden                           |
| `Array.IndexOf(array, val)` | Devuelve el índice de un valor              |
| `Array.Clear(array, i, n)`  | Limpia `n` elementos desde la posición `i`  |
| `array.Length`              | Devuelve la cantidad total de elementos     |
| `array.Rank`                | Devuelve el número de dimensiones del array |
| `Array.Copy()`              | Copia elementos entre arrays                |

🧩 Ejemplo:

```csharp
int[] numeros = { 5, 3, 8, 1 };
Array.Sort(numeros);
Console.WriteLine(string.Join(", ", numeros)); // 1, 3, 5, 8
```

---

### 🔹 17.7.- Copiar y clonar matrices

```csharp
int[] original = { 1, 2, 3 };
int[] copia = (int[])original.Clone();

copia[0] = 99;

Console.WriteLine(original[0]); // 1
Console.WriteLine(copia[0]);    // 99
```

🧠 `Clone()` crea una **copia independiente** del array.

---

### 🔹 17.8.- Uso avanzado: inicialización dinámica

Puedes crear matrices con valores calculados en tiempo de ejecución:

```csharp
int tamaño = 5;
int[] cuadrados = new int[tamaño];

for (int i = 0; i < tamaño; i++)
{
    cuadrados[i] = i * i;
}

Console.WriteLine(string.Join(", ", cuadrados)); // 0, 1, 4, 9, 16
```

---

### 🔹 17.9.- Buenas prácticas con arrays

✅ Usa `foreach` para recorrer si no necesitas el índice.
✅ Usa `Length` en lugar de números fijos.
✅ Si el tamaño del conjunto cambia con frecuencia, **usa `List<T>`** (veremos más adelante).
✅ Prefiere arrays de tipos simples (int, float, double, char, etc.) para mejor rendimiento.
⚠️ Evita indexar fuera del rango.

---

### 🔹 17.10.- Ejemplo completo

```csharp
int[,] tabla = new int[3, 3];

// Llenar la matriz
for (int i = 0; i < 3; i++)
{
    for (int j = 0; j < 3; j++)
    {
        tabla[i, j] = (i + 1) * (j + 1);
    }
}

// Mostrar resultados
for (int i = 0; i < 3; i++)
{
    for (int j = 0; j < 3; j++)
    {
        Console.Write($"{tabla[i, j],3}");
    }
    Console.WriteLine();
}
```

🧮 Resultado:

```Yaml
  1  2  3
  2  4  6
  3  6  9
```

---

### 🧠 Resumen del tema

| Tipo de array      | Ejemplo de declaración      | Característica principal              |
| ------------------ | --------------------------- | ------------------------------------- |
| Unidimensional     | `int[] a = new int[5];`     | Lista lineal de datos                 |
| Bidimensional      | `int[,] m = new int[2,3];`  | Tipo tabla (filas y columnas)         |
| Jagged (irregular) | `int[][] j = new int[3][];` | Cada fila puede tener distinto tamaño |

---

Perfecto 😎, aquí tienes la **complementación del tema 17 (Matrices)** enfocada **solo en lo que faltaba**: los **arreglos dinámicos, jagged arrays, multidimensionales, y diferencias clave entre ellos**, sin repetir lo anterior.

---

### 🔹 17.11.- Tipos de Arreglos y Variantes Avanzadas

#### 🧩 1. Arreglos Multidimensionales (`[,]`)

Son como tablas: **todas las filas tienen el mismo tamaño**.

```csharp
int[,] matriz = new int[2, 3]
{
    { 1, 2, 3 },
    { 4, 5, 6 }
};
```

Acceso:

```csharp
Console.WriteLine(matriz[1, 2]); // 6
```

Recorrido:

```csharp
for (int fila = 0; fila < matriz.GetLength(0); fila++)
{
    for (int col = 0; col < matriz.GetLength(1); col++)
    {
        Console.Write(matriz[fila, col] + " ");
    }
    Console.WriteLine();
}
```

🧠 **Uso típico:** cuando necesitas una estructura de tabla fija, como un tablero, mapa, o matriz matemática.
⚙️ **Ventaja:** muy compacto en memoria.
📉 **Desventaja:** todos los renglones deben tener igual tamaño.

---

#### 🪜 2. Arreglos Jagged (`[][]`)

También llamados **“arreglos dentados” o “irregulares”**, son **arreglos de arreglos**, permitiendo diferentes longitudes por fila.

```csharp
int[][] jagged = new int[3][];
jagged[0] = new int[] { 1, 2, 3 };
jagged[1] = new int[] { 4, 5 };
jagged[2] = new int[] { 6, 7, 8, 9 };
```

Recorrido:

```csharp
for (int i = 0; i < jagged.Length; i++)
{
    for (int j = 0; j < jagged[i].Length; j++)
    {
        Console.Write(jagged[i][j] + " ");
    }
    Console.WriteLine();
}
```

🧠 **Uso típico:** estructuras donde cada fila tiene diferente cantidad de datos (por ejemplo, notas de alumnos con distinto número de calificaciones).
⚙️ **Ventaja:** más flexible y eficiente en memoria si las filas varían mucho.
📉 **Desventaja:** acceso un poco más lento, porque cada fila es un array independiente.

---

#### 🔄 3. Arreglos Dinámicos (`List<T>`)

Los **arrays normales no cambian de tamaño**, pero con `List<T>` puedes **agregar o quitar elementos libremente**.

```csharp
List<int> numeros = new List<int>();
numeros.Add(10);
numeros.Add(20);
numeros.Add(30);
numeros.Remove(20);
```

🧠 **Uso típico:** cuando no sabes cuántos elementos tendrás al inicio.
⚙️ **Ventaja:** se ajusta automáticamente en tamaño.
📉 **Desventaja:** usa un poco más de memoria que un array fijo.

---

#### ⚡ 4. Conversión entre Arrays y Listas

Puedes convertir entre ambos fácilmente:

```csharp
int[] arreglo = { 1, 2, 3 };
List<int> lista = arreglo.ToList();

int[] nuevoArreglo = lista.ToArray();
```

---

#### 🧠 5. Redimensionar Arrays Manualmente

Si **de verdad** necesitas cambiar el tamaño de un array, puedes usar:

```csharp
Array.Resize(ref arreglo, 10); // Cambia el tamaño del arreglo
```

> ⚠️ Pero esto **crea una nueva copia en memoria**, así que no se recomienda para uso intensivo.
> Si necesitas agregar o quitar elementos constantemente, **usa una `List<T>`**.

---

#### 🔍 6. Arreglos con Tipos Personalizados

Puedes almacenar **cualquier tipo**, incluso clases u objetos:

```csharp
class Persona
{
    public string Nombre;
    public int Edad;
}

Persona[] personas = new Persona[]
{
    new Persona { Nombre = "Ana", Edad = 25 },
    new Persona { Nombre = "Luis", Edad = 30 }
};
```

---

#### ⚙️ 7. Tips de Optimización

- Usa `for` en lugar de `foreach` si necesitas máxima velocidad.
- Declara el tamaño correcto al inicio para evitar redimensiones.
- Para datos masivos, considera `Span<T>` o `Memory<T>` (altas prestaciones).
- Evita arreglos con más de 3 dimensiones: se vuelven lentos y difíciles de mantener.
- En matrices grandes, **prefiere los jagged arrays** por eficiencia en acceso y memoria.

Perfecto 😎🔥 entonces el **siguiente tema será:**

---

## 🧱 18.- Listas y Colecciones en C #

Aquí empezaremos a subir de nivel: pasamos de los **arreglos estáticos** (tamaño fijo) a las **colecciones dinámicas** del *namespace* `System.Collections.Generic`, que son el corazón de la manipulación de datos moderna en C#.

Estas estructuras permiten **agregar, eliminar, buscar y ordenar** elementos fácilmente, sin tener que preocuparnos por manejar índices manuales ni tamaños fijos.

---

### 🧩 18.1.- Introducción a las Colecciones Genéricas

- Las colecciones son estructuras de datos **dinámicas** que almacenan grupos de elementos.
- Las colecciones **genéricas** (como `List<T>`, `Dictionary<TKey, TValue>`, etc.) permiten especificar el tipo de dato, mejorando la seguridad y el rendimiento.

```csharp
List<int> numeros = new List<int>();
numeros.Add(10);
numeros.Add(20);
numeros.Add(30);
```

📘 **Ventaja:** C# evita conversiones de tipo innecesarias, haciendo el código más rápido y seguro.

---

### 📋 18.2.- List<T> — Listas Dinámicas

La clase `List<T>` es la **evolución directa de los arreglos**.
Permite crecer o disminuir en tamaño automáticamente.

```csharp
List<string> nombres = new List<string> { "Ana", "Luis", "Pedro" };
nombres.Add("Lucía");
nombres.Remove("Luis");
```

**Métodos comunes:**

| Método       | Descripción                     |
| ------------ | ------------------------------- |
| `Add()`      | Agrega un elemento              |
| `Remove()`   | Elimina un elemento             |
| `Insert()`   | Inserta en posición específica  |
| `Contains()` | Comprueba si existe un elemento |
| `Sort()`     | Ordena la lista                 |
| `Clear()`    | Vacía la lista                  |

🧠 **Tip:** si necesitas agregar millones de elementos, inicializa la lista con capacidad estimada para mejorar el rendimiento:

```csharp
List<int> listaGrande = new List<int>(1000000);
```

---

### 🔑 18.3.- Dictionary<TKey, TValue> — Diccionarios (Mapas Clave-Valor)

El `Dictionary` asocia **una clave única con un valor**, ideal para búsquedas rápidas.

```csharp
Dictionary<string, int> edades = new Dictionary<string, int>();
edades["Ana"] = 25;
edades["Luis"] = 30;

Console.WriteLine(edades["Luis"]); // 30
```

**Métodos útiles:**

| Método                        | Descripción                   |
| ----------------------------- | ----------------------------- |
| `Add(key, value)`             | Agrega un par clave-valor     |
| `Remove(key)`                 | Elimina una clave             |
| `ContainsKey(key)`            | Comprueba existencia de clave |
| `TryGetValue(key, out value)` | Obtiene valor de forma segura |

🧠 **Usos comunes:** tablas de configuración, catálogos, índices o conteo de ocurrencias.

---

### 📦 18.4.- Queue<T> — Colas (FIFO)

Estructura de tipo **primero en entrar, primero en salir (FIFO)**.

```csharp
Queue<string> cola = new Queue<string>();
cola.Enqueue("Cliente 1");
cola.Enqueue("Cliente 2");

string atendido = cola.Dequeue();
Console.WriteLine(atendido); // Cliente 1
```

| Método      | Descripción                             |
| ----------- | --------------------------------------- |
| `Enqueue()` | Agrega un elemento al final             |
| `Dequeue()` | Extrae el primer elemento               |
| `Peek()`    | Muestra el primer elemento sin quitarlo |

🧠 **Uso típico:** simulaciones, sistemas de turnos, o procesos por orden de llegada.

---

### 🪃 18.5.- Stack<T> — Pilas (LIFO)

Estructura **último en entrar, primero en salir (LIFO)**.
Imagina una pila de platos: el último que pones es el primero que sacas.

```csharp
Stack<int> pila = new Stack<int>();
pila.Push(10);
pila.Push(20);
int ultimo = pila.Pop(); // 20
```

| Método   | Descripción                       |
| -------- | --------------------------------- |
| `Push()` | Agrega un elemento arriba         |
| `Pop()`  | Saca el elemento superior         |
| `Peek()` | Consulta el superior sin quitarlo |

🧠 **Uso común:** deshacer/rehacer, navegación atrás/adelante, llamadas recursivas.

---

### 🔍 18.6.- HashSet<T> — Conjuntos sin duplicados

Guarda elementos **únicos**, sin repetición y sin orden definido.

```csharp
HashSet<int> numeros = new HashSet<int> { 1, 2, 2, 3 };
Console.WriteLine(string.Join(", ", numeros)); // 1, 2, 3
```

| Método            | Descripción          |
| ----------------- | -------------------- |
| `Add()`           | Agrega si no existe  |
| `Remove()`        | Elimina              |
| `Contains()`      | Comprueba si existe  |
| `UnionWith()`     | Une dos conjuntos    |
| `IntersectWith()` | Obtiene intersección |

🧠 **Uso típico:** evitar duplicados en listas o filtrar elementos únicos.

---

### 🧮 18.7.- SortedList y SortedDictionary

Son versiones **ordenadas automáticamente** de `List` y `Dictionary`.

```csharp
SortedList<int, string> listaOrdenada = new SortedList<int, string>();
listaOrdenada.Add(3, "Tres");
listaOrdenada.Add(1, "Uno");
listaOrdenada.Add(2, "Dos");
```

📘 **Resultado:** siempre ordenado por clave → 1, 2, 3.

---

### 🧠 18.8.- Consejos y Buenas Prácticas

- Usa `List<T>` para la mayoría de los casos generales.
- Usa `Dictionary<TKey, TValue>` cuando necesites búsquedas rápidas por clave.
- Usa `HashSet<T>` si necesitas **un conjunto sin duplicados**.
- Evita convertir entre colecciones constantemente (usa la correcta desde el inicio).
- Usa `foreach` para recorrer colecciones legibles y seguras.
- En operaciones masivas, preasigna capacidad para evitar realocaciones.

---

### 💡 18.9.- Ejemplo Práctico: Gestión de Estudiantes

```csharp
List<string> alumnos = new List<string> { "Ana", "Luis", "Pedro" };
Dictionary<string, int> calificaciones = new Dictionary<string, int>()
{
    { "Ana", 95 },
    { "Luis", 80 },
    { "Pedro", 88 }
};

foreach (var alumno in alumnos)
{
    Console.WriteLine($"{alumno} tiene {calificaciones[alumno]} puntos.");
}
```

**Salida:**

```yaml
Ana tiene 95 puntos.
Luis tiene 80 puntos.
Pedro tiene 88 puntos.
```

Perfecto 😎🔥
Entonces seguimos con el tema **## 19.- Métodos en C#**, uno de los pilares fundamentales de la programación estructurada y orientada a objetos.
Aquí aprenderás a **crear, usar, sobrecargar y optimizar** tus propios métodos para escribir código más limpio, reutilizable y profesional.

---

## 🧩 19.- Métodos en C #

### 19.1 ¿Qué es un Método?

Un **método** es un bloque de código que ejecuta una tarea específica y puede devolver un valor.
Sirve para **evitar repetir código** y hacer el programa más legible y modular.

```csharp
void Saludar()
{
    Console.WriteLine("¡Hola LechuDev!");
}
```

📘 **Se ejecuta** cuando lo llamas:

```csharp
Saludar();
```

---

### 19.2 Estructura de un Método

```csharp
[Modificador] [TipoRetorno] [Nombre]([Parámetros])
{
    // Cuerpo del método
}
```

**Ejemplo:**

```csharp
public int Sumar(int a, int b)
{
    return a + b;
}
```

| Elemento         | Descripción                                                              |
| ---------------- | ------------------------------------------------------------------------ |
| `public`         | Modificador de acceso (puede ser `public`, `private`, `protected`, etc.) |
| `int`            | Tipo de dato que devuelve el método                                      |
| `Sumar`          | Nombre del método                                                        |
| `(int a, int b)` | Parámetros de entrada                                                    |
| `return a + b;`  | Valor que devuelve el método                                             |

---

### 19.3 Métodos `void` (sin retorno)

Los métodos `void` **no devuelven ningún valor**, solo ejecutan una acción.

```csharp
void MostrarMensaje(string mensaje)
{
    Console.WriteLine(mensaje);
}

MostrarMensaje("Hola desde un método!");
```

---

### 19.4 Métodos con Retorno

Devuelven un valor del tipo indicado.
Se utiliza `return` para devolver el resultado.

```csharp
int Cuadrado(int numero)
{
    return numero * numero;
}

int resultado = Cuadrado(5);
Console.WriteLine(resultado); // 25
```

---

### 19.5 Parámetros y Argumentos

Un **parámetro** es una variable declarada en la definición del método.
Un **argumento** es el valor que se pasa al llamar al método.

```csharp
void SaludoPersonalizado(string nombre)
{
    Console.WriteLine($"Hola, {nombre}!");
}

SaludoPersonalizado("LechuDev"); // argumento = "LechuDev"
```

---

### 19.6 Parámetros por Valor y por Referencia

#### 🔹 Por Valor (default)

Se pasa una **copia** del valor.

```csharp
void Incrementar(int x)
{
    x++;
}
int numero = 10;
Incrementar(numero);
Console.WriteLine(numero); // 10 (no cambió)
```

#### 🔹 Por Referencia (`ref`)

Permite modificar la variable original.

```csharp
void IncrementarRef(ref int x)
{
    x++;
}
int numero = 10;
IncrementarRef(ref numero);
Console.WriteLine(numero); // 11
```

#### 🔹 Solo salida (`out`)

Permite devolver **más de un valor** sin usar clases o tuplas.

```csharp
void Calcular(int a, int b, out int suma, out int resta)
{
    suma = a + b;
    resta = a - b;
}
Calcular(8, 3, out int s, out int r);
Console.WriteLine($"Suma: {s}, Resta: {r}");
```

---

### 19.7 Parámetros Opcionales y con Nombre

```csharp
void MostrarDatos(string nombre, int edad = 18)
{
    Console.WriteLine($"{nombre} tiene {edad} años.");
}

MostrarDatos("LechuDev");       // usa edad por defecto = 18
MostrarDatos("Carlos", 25);     // edad = 25
MostrarDatos(edad: 30, nombre: "Ana"); // parámetros con nombre
```

---

### 19.8 Métodos Estáticos (`static`)

Los métodos estáticos **pertenecen a la clase**, no a una instancia.

```csharp
class Calculadora
{
    public static int Sumar(int a, int b) => a + b;
}

int resultado = Calculadora.Sumar(4, 6);
Console.WriteLine(resultado);
```

🧠 **Uso común:** cuando el método no depende de datos del objeto, solo realiza una operación.

---

### 19.9 Sobrecarga de Métodos (Overloading)

Puedes tener **varios métodos con el mismo nombre**, siempre que los parámetros sean distintos.

```csharp
int Sumar(int a, int b) => a + b;
double Sumar(double a, double b) => a + b;
```

🧠 **El compilador elige** el método correcto según el tipo de datos que reciba.

---

### 19.10 Expresiones Lambda (Métodos en una línea)

Una **expresión lambda** simplifica la sintaxis de un método.

```csharp
int Cuadrado(int n) => n * n;
```

Es equivalente a:

```csharp
int Cuadrado(int n)
{
    return n * n;
}
```

---

### 19.11 Métodos Locales (anidados dentro de otro método)

Desde C# 7 puedes declarar métodos **dentro de otros métodos**.

```csharp
void Proceso()
{
    int Calcular(int x) => x * 2;
    Console.WriteLine(Calcular(5));
}

Proceso(); // 10
```

---

### 19.12 Métodos Asíncronos (`async` / `await`)

Permiten ejecutar tareas sin bloquear el programa principal.

```csharp
async Task DescargarAsync()
{
    await Task.Delay(2000); // simula espera
    Console.WriteLine("Descarga completa!");
}

await DescargarAsync();
```

🧠 **Uso:** ideal para peticiones web, lectura de archivos, o procesos lentos.

---

### 19.13 Buenas Prácticas

✅ Usa nombres descriptivos y en PascalCase (`CalcularPromedio`).
✅ Evita métodos muy largos: si un método hace más de una cosa, divídelo.
✅ Prefiere **`return` temprano** para evitar bloques anidados.
✅ Documenta parámetros y retornos con comentarios XML si trabajas en equipo.

---

### 19.14 Ejemplo Final: Calculadora Modular

```csharp
class Calculadora
{
    public static int Sumar(int a, int b) => a + b;
    public static int Restar(int a, int b) => a - b;
    public static int Multiplicar(int a, int b) => a * b;
    public static double Dividir(double a, double b) => b != 0 ? a / b : double.NaN;
}

Console.WriteLine(Calculadora.Sumar(4, 5));
Console.WriteLine(Calculadora.Restar(10, 3));
Console.WriteLine(Calculadora.Multiplicar(2, 6));
Console.WriteLine(Calculadora.Dividir(8, 2));
```

📘 **Salida:**

```yaml
9
7
12
4
```

---

Perfecto 😎🔥
Sigamos entonces con el tema **## 20.- Métodos y Funciones Avanzadas en C#**, donde conectaremos todo lo aprendido con conceptos más poderosos y flexibles de programación.

---

## 🧩 20.- Métodos y Funciones Avanzadas

### 20.1 Recursividad

Un **método recursivo** es aquel que **se llama a sí mismo**.
Se utiliza para problemas que se pueden dividir en subproblemas similares.

```csharp
int Factorial(int n)
{
    if (n <= 1) return 1;
    return n * Factorial(n - 1);
}

Console.WriteLine(Factorial(5)); // 120
```

💡 **Reglas:**

- Debe existir una **condición base** para evitar bucles infinitos.
- Útil para: factorial, Fibonacci, búsqueda en árboles, algoritmos de backtracking.

---

### 20.2 Funciones Anónimas (Anonymous Functions)

Son funciones sin nombre, usadas generalmente en **delegados o eventos**.

```csharp
Func<int, int> cuadrado = delegate(int x) { return x * x; };
Console.WriteLine(cuadrado(6)); // 36
```

---

### 20.3 Expresiones Lambda Avanzadas

Simplifican aún más las funciones anónimas.

```csharp
Func<int, int> doble = x => x * 2;
Func<int, int, int> suma = (a, b) => a + b;

Console.WriteLine(doble(5)); // 10
Console.WriteLine(suma(3, 4)); // 7
```

💡 **Tip:** ideales para filtros, ordenamientos y LINQ.

---

### 20.4 Delegados (Delegates)

Un **delegado** es un tipo que **referencia métodos**.
Permite pasar funciones como parámetros y crear callbacks.

```csharp
delegate int Operacion(int a, int b);

int Sumar(int x, int y) => x + y;
int Multiplicar(int x, int y) => x * y;

Operacion op = Sumar;
Console.WriteLine(op(3, 4)); // 7

op = Multiplicar;
Console.WriteLine(op(3, 4)); // 12
```

💡 **Ventaja:** permite desacoplar código y programar patrones como Observer.

---

### 20.5 Eventos (basados en Delegados)

Los eventos permiten **notificar cambios o acciones**.

```csharp
class Publicador
{
    public event Action EventoMensaje;

    public void LanzarEvento()
    {
        EventoMensaje?.Invoke();
    }
}

var p = new Publicador();
p.EventoMensaje += () => Console.WriteLine("¡Evento disparado!");
p.LanzarEvento(); // ¡Evento disparado!
```

---

### 20.6 Métodos Genéricos

Permiten crear **métodos que funcionan con cualquier tipo de dato**.

```csharp
T ObtenerValor<T>(T valor)
{
    return valor;
}

Console.WriteLine(ObtenerValor<int>(42));      // 42
Console.WriteLine(ObtenerValor<string>("Hola")); // Hola
```

💡 **Tip:** combinable con `List<T>` y colecciones genéricas.

---

### 20.7 Parámetros `params`

Permiten pasar **un número variable de argumentos** a un método.

```csharp
int SumarTodos(params int[] numeros)
{
    int suma = 0;
    foreach (var n in numeros)
        suma += n;
    return suma;
}

Console.WriteLine(SumarTodos(1, 2, 3, 4)); // 10
```

---

### 20.8 Métodos de Extensión

Permiten **añadir métodos a clases existentes** sin herencia ni modificar su código.

```csharp
public static class Extensiones
{
    public static bool EsPar(this int n) => n % 2 == 0;
}

int numero = 8;
Console.WriteLine(numero.EsPar()); // True
```

💡 **Uso:** muy común en LINQ y utilidades de manipulación de datos.

---

### 20.9 Métodos Asíncronos Avanzados

Combina `async`, `await` y `Task` para **procesos paralelos o I/O sin bloqueo**.

```csharp
async Task<int> ObtenerDatosAsync()
{
    await Task.Delay(2000); // Simula descarga
    return 42;
}

int valor = await ObtenerDatosAsync();
Console.WriteLine(valor); // 42
```

💡 **Tip:** evita `Thread.Sleep` en interfaces gráficas o servidores.

---

### 20.10 Buenas Prácticas

- Mantén **un método = una responsabilidad**.
- Usa **delegados y eventos** para desacoplar código.
- Prefiere **métodos genéricos** y de extensión para reutilización.
- Evita recursión profunda sin optimización: usa recursión de cola o bucles si es masiva.
- Documenta parámetros, retornos y excepciones.

---

### 20.11 Ejemplo Integrado: Calculadora Genérica y Asíncrona

```csharp
class Calculadora
{
    public static async Task<double> OperarAsync(double a, double b, Func<double, double, double> op)
    {
        await Task.Delay(500); // simulación de procesamiento
        return op(a, b);
    }
}

double suma = await Calculadora.OperarAsync(5, 3, (x, y) => x + y);
double multi = await Calculadora.OperarAsync(5, 3, (x, y) => x * y);

Console.WriteLine($"Suma: {suma}, Multiplicación: {multi}");
```

**Salida:**

```yaml
Suma: 8, Multiplicación: 15
```

¡Perfecto! Vamos a explicarlo paso a paso, con un enfoque **muy amigable para novatos**, usando ejemplos claros y desglosando cada concepto. Vamos a desarrollar el tema **21.- Delegados, Eventos y LINQ**.

---

## 21.- Delegados, Eventos y LINQ en C#**

### 21.1 ¿Qué es un Delegado?

Un **delegado** es como un **teléfono que puede llamar a un método**.
En otras palabras, un delegado **guarda la referencia de un método** y permite ejecutarlo después, o pasarlo como parámetro a otro método.

📌 **Para qué sirve:**

- Permite que tu código sea más flexible y reutilizable.
- Permite pasar un método como si fuera un dato (esto es muy útil para callbacks o eventos).

#### Ejemplo Básico

```csharp
// Declaración del delegado
delegate void SaludoDelegado(string nombre);

// Método que coincide con la firma del delegado
void Saludar(string nombre)
{
    Console.WriteLine($"Hola, {nombre}!");
}

// Usando el delegado
SaludoDelegado miDelegado = Saludar;
miDelegado("LechuDev"); // Llama al método Saludar
```

**Explicación:**

- `delegate void SaludoDelegado(string nombre);` → Define un tipo de delegado que apunta a métodos que reciben un string y no devuelven nada.
- `miDelegado("LechuDev");` → Ejecuta el método apuntado por el delegado.

---

### 21.2 Delegados Multicast

Un delegado puede **apuntar a varios métodos** al mismo tiempo.

```csharp
void Saludar(string nombre) => Console.WriteLine($"Hola, {nombre}!");
void Despedir(string nombre) => Console.WriteLine($"Adiós, {nombre}!");

SaludoDelegado miDelegado = Saludar;
miDelegado += Despedir; // Agrega otro método

miDelegado("LechuDev"); 
```

**Salida:**

```yaml
Hola, LechuDev!
Adiós, LechuDev!
```

💡 **Tip:** Se usa para notificaciones o ejecutar varias acciones con un solo delegado.

---

### 21.3 Eventos

Un **evento** es una **señal que un objeto envía** cuando sucede algo importante.
Los objetos que quieren reaccionar a ese evento **se suscriben** a él mediante delegados.

#### Ejemplo Básico de Eventos

```csharp
class Boton
{
    public event Action AlHacerClick;

    public void HacerClick()
    {
        AlHacerClick?.Invoke(); // Lanza el evento si alguien está suscrito
    }
}

// Suscribirse al evento
Boton boton = new Boton();
boton.AlHacerClick += () => Console.WriteLine("¡Botón presionado!");
boton.HacerClick();
```

**Explicación paso a paso:**

- `public event Action AlHacerClick;` → Define un evento basado en el delegado `Action`.
- `boton.AlHacerClick += ...` → Se suscribe un método (en este caso lambda) al evento.
- `AlHacerClick?.Invoke();` → Dispara el evento; todos los suscriptores se ejecutan.

💡 **Tip:** Los eventos se usan muchísimo en interfaces gráficas, juegos y notificaciones.

---

### 21.4 Delegados Genéricos (`Func` y `Action`)

C# tiene **delegados predefinidos** para evitar escribir tipos nuevos todo el tiempo.

- `Action` → No devuelve nada, puede recibir parámetros.
- `Func<T, TResult>` → Devuelve un valor (`TResult`), puede recibir parámetros.

```csharp
Action<string> saludar = nombre => Console.WriteLine($"Hola, {nombre}!");
saludar("LechuDev");

Func<int, int, int> sumar = (a, b) => a + b;
Console.WriteLine(sumar(5, 3)); // 8
```

---

### 21.5 LINQ (Language Integrated Query)

**LINQ** permite **consultar colecciones de datos** (listas, arrays, bases de datos) de forma sencilla y declarativa, como si fuera SQL.

#### Ejemplo básico

```csharp
List<int> numeros = new List<int> { 1, 2, 3, 4, 5, 6 };

// Filtrar números pares
var pares = numeros.Where(n => n % 2 == 0);

foreach (var n in pares)
{
    Console.WriteLine(n);
}
```

**Salida:**

```yaml
2
4
6
```

💡 **Explicación:**

- `Where` recibe un **predicado** (una función que devuelve true o false) y selecciona los elementos que cumplen la condición.
- El `=>` es la **expresión lambda**, que define la función en una línea.

---

### 21.6 Operadores LINQ Comunes

| Operador                   | Qué hace                                                  |
| -------------------------- | --------------------------------------------------------- |
| `Where`                    | Filtra elementos según una condición                      |
| `Select`                   | Proyecta o transforma elementos                           |
| `OrderBy`                  | Ordena de forma ascendente                                |
| `OrderByDescending`        | Ordena de forma descendente                               |
| `First` / `FirstOrDefault` | Obtiene el primer elemento (o valor por defecto)          |
| `Last` / `LastOrDefault`   | Obtiene el último elemento                                |
| `Count`                    | Cuenta elementos                                          |
| `Sum` / `Average`          | Suma o calcula promedio                                   |
| `Any`                      | Devuelve true si al menos un elemento cumple la condición |
| `All`                      | Devuelve true si todos los elementos cumplen la condición |

#### Ejemplo usando varios

```csharp
var resultado = numeros
                .Where(n => n > 2)
                .OrderByDescending(n => n)
                .Select(n => n * 10);

foreach (var n in resultado)
    Console.WriteLine(n);
```

**Salida:**

```yaml
60
50
40
30
```

---

### 21.7 Buenas Prácticas para Delegados, Eventos y LINQ

✅ Usa **delegados genéricos** (`Func` y `Action`) cuando puedas.
✅ Evita eventos con muchas suscripciones innecesarias; limpia suscriptores si ya no se usan.
✅ Usa LINQ para **consultas claras y legibles**, pero cuidado con colecciones muy grandes: evalúa rendimiento.
✅ Prefiere expresiones lambda pequeñas y descriptivas.
✅ Documenta qué hace cada evento y delegado.

---

## 22.- Programación Orientada a Objetos (POO) en C #

La **POO** es un paradigma de programación que organiza el código mediante **objetos**, que son instancias de **clases**, permitiendo modelar el mundo real dentro de un programa.

C# es un lenguaje **totalmente orientado a objetos**, por lo que aprender POO es esencial para programar profesionalmente.

---

### 22.1 Conceptos Clave

1. **Clase:** Es un **molde o plantilla** que define las propiedades (datos) y métodos (funciones) de un objeto.
2. **Objeto:** Es una **instancia de una clase**, es decir, un “ejemplar” concreto con valores propios.
3. **Propiedad (Property):** Una variable dentro de la clase que describe el estado de un objeto.
4. **Método (Method):** Una función dentro de la clase que describe el comportamiento del objeto.
5. **Encapsulamiento:** Ocultar datos internos y controlar el acceso a ellos mediante métodos o propiedades.
6. **Herencia:** Permite crear nuevas clases basadas en clases existentes, reutilizando código.
7. **Polimorfismo:** La capacidad de que un objeto se comporte de diferentes formas según el contexto.
8. **Abstracción:** Simplificación del mundo real mostrando solo lo necesario y ocultando los detalles internos.

---

### 22.2 Clases y Objetos

#### 22.2.1 Declaración de una Clase

```csharp
class Persona
{
    // Propiedades
    public string Nombre;
    public int Edad;

    // Método
    public void Saludar()
    {
        Console.WriteLine($"Hola, soy {Nombre} y tengo {Edad} años.");
    }
}
```

#### 22.2.2 Crear un Objeto

```csharp
Persona p1 = new Persona();
p1.Nombre = "Lechu";
p1.Edad = 28;
p1.Saludar(); // "Hola, soy Lechu y tengo 28 años."
```

**Explicación:**

- `class Persona { ... }` → Define una clase llamada `Persona`.
- `Persona p1 = new Persona();` → Crea un objeto `p1` de la clase `Persona`.
- `p1.Nombre = "Lechu";` → Asigna valor a la propiedad del objeto.

---

### 22.3 Constructores

Un **constructor** es un método especial que se ejecuta **al crear un objeto**, usado para inicializar propiedades.

```csharp
class Persona
{
    public string Nombre;
    public int Edad;

    // Constructor
    public Persona(string nombre, int edad)
    {
        Nombre = nombre;
        Edad = edad;
    }

    public void Saludar()
    {
        Console.WriteLine($"Hola, soy {Nombre} y tengo {Edad} años.");
    }
}

// Crear objeto usando constructor
Persona p2 = new Persona("LechuDev", 28);
p2.Saludar();
```

**Tip:** Puedes tener varios constructores con **diferentes parámetros** (sobrecarga de constructores).

---

### 22.4 Propiedades y Encapsulamiento

En lugar de usar variables públicas, podemos usar **propiedades con get y set**:

```csharp
class Persona
{
    private int edad; // Variable privada

    public string Nombre { get; set; } // Auto-propiedad

    public int Edad
    {
        get { return edad; }
        set
        {
            if (value >= 0) edad = value; // Validación
            else Console.WriteLine("Edad inválida");
        }
    }
}

Persona p = new Persona();
p.Nombre = "LechuDev";
p.Edad = 28;
Console.WriteLine($"{p.Nombre} tiene {p.Edad} años.");
```

**Explicación:**

- `Nombre { get; set; }` → Propiedad pública simple.
- `Edad` → Propiedad con **validación**, que protege la integridad del dato.
- Esto es **encapsulamiento**, ocultando la variable `edad`.

---

### 22.5 Métodos

- Los métodos definen **comportamiento**.
- Pueden tener **parámetros** y **devolver valores**.

```csharp
class Calculadora
{
    public int Sumar(int a, int b)
    {
        return a + b;
    }
}

Calculadora calc = new Calculadora();
Console.WriteLine(calc.Sumar(5, 3)); // 8
```

💡 Buen hábito: los métodos deben **hacer solo una cosa**, ser **claros y cortos**.

---

### 22.6 Herencia

La herencia permite **crear una clase basada en otra**, reutilizando código.

```csharp
class Animal
{
    public void Comer() => Console.WriteLine("Comiendo...");
}

class Perro : Animal
{
    public void Ladrar() => Console.WriteLine("Guau!");
}

Perro miPerro = new Perro();
miPerro.Comer(); // Heredado
miPerro.Ladrar(); // Propio
```

**Tip:** Usa herencia para **evitar repetir código** y crear jerarquías lógicas.

---

### 22.7 Polimorfismo

El polimorfismo permite que **un mismo método se comporte de manera distinta** según la clase que lo implemente.

```csharp
class Animal
{
    public virtual void HacerSonido()
    {
        Console.WriteLine("Sonido genérico");
    }
}

class Perro : Animal
{
    public override void HacerSonido()
    {
        Console.WriteLine("Guau!");
    }
}

Animal a = new Perro();
a.HacerSonido(); // "Guau!" gracias al polimorfismo
```

**Explicación:**

- `virtual` → Método que puede ser sobrescrito.
- `override` → Método que sobrescribe al original en la subclase.

---

### 22.8 Abstracción

- Permite **centrarse en lo esencial** y ocultar los detalles internos.
- Se logra usando **clases abstractas** o **interfaces**.

```csharp
abstract class Figura
{
    public abstract double Area(); // Método sin implementación
}

class Circulo : Figura
{
    public double Radio { get; set; }
    public override double Area() => Math.PI * Radio * Radio;
}

Circulo c = new Circulo { Radio = 3 };
Console.WriteLine(c.Area()); // 28.27
```

**Tip:** Usa abstracción para **definir contratos claros** sin exponer detalles innecesarios.

---

### 22.9 Interfaces

- Son **contratos** que las clases deben implementar.
- Una clase puede implementar **múltiples interfaces**, pero solo heredar de una clase.

```csharp
interface IVehículo
{
    void Conducir();
}

class Coche : IVehículo
{
    public void Conducir()
    {
        Console.WriteLine("Conduciendo el coche");
    }
}

IVehiculo miCoche = new Coche();
miCoche.Conducir();
```

---

### 22.10 Buenas Prácticas en POO

1. Siempre usa **encapsulamiento** (`private` + `get/set`).
2. Evita **herencias profundas**; prefiere composición si es posible.
3. Implementa **interfaces** para flexibilizar tu código.
4. Mantén tus clases **pequeñas y cohesionadas**: cada clase hace una sola cosa.
5. Usa **constructores y sobrecarga** para inicializar objetos claramente.
6. Aplica **polimorfismo y abstracción** para mejorar mantenibilidad.

---

---

## Indice

- [Curso de Programación en C](#curso-de-programación-en-c)
  - [Introducción](#introducción)
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
      - [3.1.1 Versión Antigua (C# 1.0 - 7.0)](#311-versión-antigua-c-10---70)
      - [3.1.2 Versión Moderna (C# 9 y superior)](#312-versión-moderna-c-9-y-superior)
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
    - [5.8 Variables locales y globales](#58-variables-locales-y-globales)
      - [5.8.1 Variables Locales](#581-variables-locales)
        - [Ejemplo](#ejemplo)
      - [5.8.2 Variables Globales (Campos / Variables de Clase)](#582-variables-globales-campos--variables-de-clase)
        - [Ejemplo de Variables Globales](#ejemplo-de-variables-globales)
      - [5.8.3 Buenas Prácticas](#583-buenas-prácticas)
    - [5.9 Variables Privadas y Públicas](#59-variables-privadas-y-públicas)
      - [5.9.1 Variables Públicas (`public`)](#591-variables-públicas-public)
        - [Ejemplo Variables Públicas](#ejemplo-variables-públicas)
      - [5.9.2 Variables Privadas (`private`)](#592-variables-privadas-private)
        - [Ejemplo Variables privadas](#ejemplo-variables-privadas)
      - [5.9.3 Buenas Prácticas](#593-buenas-prácticas)
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
  - [7.- Los Operadores en C](#7--los-operadores-en-c)
    - [7.1.- Operadores Aritméticos](#71--operadores-aritméticos)
      - [7.1.1.- Suma (`+`)](#711--suma-)
      - [7.1.2 Resta (`-`)](#712-resta--)
      - [7.1.3 Multiplicación (`*`)](#713-multiplicación-)
      - [7.1.4 División (`/`)](#714-división-)
      - [7.1.5 Módulo (`%`)](#715-módulo-)
      - [7.1.6 Incremento (`++`)](#716-incremento-)
      - [7.1.7 Decremento (`--`)](#717-decremento---)
      - [7.1.8 Exponenciación (potencias)](#718-exponenciación-potencias)
      - [7.1.9 Resumen](#719-resumen)
      - [7.1.10 Ejemplo: Calculadora simple](#7110-ejemplo-calculadora-simple)
    - [7.2.- Operadores de Asignación](#72--operadores-de-asignación)
      - [🔹 7.2.1 Asignación básica (`=`)](#-721-asignación-básica-)
      - [🔹 7.2.2 Asignación con suma (`+=`)](#-722-asignación-con-suma-)
      - [🔹 7.2.3 Asignación con resta (`-=`)](#-723-asignación-con-resta--)
      - [🔹 7.2.4 Asignación con multiplicación (`*=`)](#-724-asignación-con-multiplicación-)
      - [🔹 7.2.5 Asignación con división (`/=`)](#-725-asignación-con-división-)
      - [🔹 7.2.6 Asignación con módulo (`%=`)](#-726-asignación-con-módulo-)
      - [🔹 7.2.7 Resumen de los operadores de asignación](#-727-resumen-de-los-operadores-de-asignación)
      - [🔹 7.2.8 Ejemplo: Calculadora avanzada](#-728-ejemplo-calculadora-avanzada)
        - [🔹 Explicación paso a paso](#-explicación-paso-a-paso)
    - [7.3.- Operadores Relacionales y de Comparación](#73--operadores-relacionales-y-de-comparación)
      - [🔹 7.3.1 Igualdad (`==`)](#-731-igualdad-)
      - [🔹 7.3.2 Diferente (`!=`)](#-732-diferente-)
      - [🔹 7.3.3 Mayor que (`>`)](#-733-mayor-que-)
      - [🔹 7.3.4 Menor que (`<`)](#-734-menor-que-)
      - [🔹 7.3.5 Mayor o igual que (`>=`)](#-735-mayor-o-igual-que-)
      - [🔹 7.3.6 Menor o igual que (`<=`)](#-736-menor-o-igual-que-)
      - [🔹 7.3.7 Ejemplo práctico: Comparaciones combinadas](#-737-ejemplo-práctico-comparaciones-combinadas)
    - [7.4.- Operadores Lógicos (`&&`, `||`, `!`)](#74--operadores-lógicos---)
      - [🔹 7.4.1 AND lógico (`&&`)](#-741-and-lógico-)
      - [🔹 7.4.2 OR lógico (`||`)](#-742-or-lógico-)
      - [🔹 7.4.3 NOT lógico (`!`)](#-743-not-lógico-)
      - [🔹 7.4.4 Combinación de operadores lógicos y relacionales](#-744-combinación-de-operadores-lógicos-y-relacionales)
      - [🔹 7.4.5 Tabla de verdad de operadores lógicos](#-745-tabla-de-verdad-de-operadores-lógicos)
      - [🔹 7.4.6 Ejemplo práctico: Control de acceso](#-746-ejemplo-práctico-control-de-acceso)
    - [7.6.- Operador de Incremento (`++`)](#76--operador-de-incremento-)
      - [🔹 Ejemplo 1: Prefijo (`++variable`)](#-ejemplo-1-prefijo-variable)
      - [🔹 Ejemplo 2: Sufijo (`variable++`)](#-ejemplo-2-sufijo-variable)
    - [7.7.- Operador de Decremento (`--`)](#77--operador-de-decremento---)
      - [🔹 Ejemplo 1: Prefijo (`--variable`)](#-ejemplo-1-prefijo---variable)
      - [🔹 Ejemplo 2: Sufijo (`variable--`)](#-ejemplo-2-sufijo-variable--)
    - [7.8.- Exponenciación (`Math.Pow`)](#78--exponenciación-mathpow)
      - [7.8.1.-🔹 Ejemplo básico de `Math.Pow`](#781--ejemplo-básico-de-mathpow)
      - [7.8.2.-🔹 Combinación con otros operadores](#782--combinación-con-otros-operadores)
      - [7.8.3🔹 Ejemplo avanzado: Validación de resultados](#783-ejemplo-avanzado-validación-de-resultados)
      - [7.8.4🔹 Resumen](#784-resumen)
    - [7.9.- Ejemplo final: Calculadora Avanzada](#79--ejemplo-final-calculadora-avanzada)
      - [🔹 7.9.1 Explicación paso a paso](#-791-explicación-paso-a-paso)
  - [8.- Transformar Cadenas a Valores Numéricos](#8--transformar-cadenas-a-valores-numéricos)
    - [8.1.- Conversión usando `int.Parse()` y `double.Parse()`](#81--conversión-usando-intparse-y-doubleparse)
    - [8.2.- Conversión segura con `TryParse()`](#82--conversión-segura-con-tryparse)
    - [8.3.- Conversión de números decimales](#83--conversión-de-números-decimales)
    - [8.4.- Conversión usando `Convert.ToInt32()` y `Convert.ToDouble()`](#84--conversión-usando-converttoint32-y-converttodouble)
    - [8.5.- Conversión a otros tipos numéricos con `Convert`](#85--conversión-a-otros-tipos-numéricos-con-convert)
    - [8.6.-Tabla de Conversiones en C](#86-tabla-de-conversiones-en-c)
  - [9.- Funciones Matemáticas de la Librería Math](#9--funciones-matemáticas-de-la-librería-math)
    - [9.1.- Raíz Cuadrada y Potencias](#91--raíz-cuadrada-y-potencias)
    - [9.2.- Valores Absolutos y Signos](#92--valores-absolutos-y-signos)
    - [9.3.- Redondeo y Truncamiento](#93--redondeo-y-truncamiento)
    - [9.4.- Mínimo, Máximo y Comparaciones](#94--mínimo-máximo-y-comparaciones)
    - [9.5.- Logaritmos y Exponenciales](#95--logaritmos-y-exponenciales)
    - [9.6.- Trigonometría](#96--trigonometría)
    - [9.8.- Raíces y Potencias Avanzadas](#98--raíces-y-potencias-avanzadas)
    - [9.9.- Funciones de Redondeo con Decimales](#99--funciones-de-redondeo-con-decimales)
    - [9.10.- Funciones de Valor Absoluto Avanzadas](#910--funciones-de-valor-absoluto-avanzadas)
    - [9.11.- Comparaciones y Clamping](#911--comparaciones-y-clamping)
    - [9.12.- Funciones Trigonométricas Adicionales](#912--funciones-trigonométricas-adicionales)
    - [9.13.- Funciones Hiperbólicas](#913--funciones-hiperbólicas)
    - [9.14.- Funciones de Comparación de Precisión](#914--funciones-de-comparación-de-precisión)
    - [9.15.- Ejemplo práctico: “Demostración completa de Math”](#915--ejemplo-práctico-demostración-completa-de-math)
      - [🔹 Qué hace este programa](#-qué-hace-este-programa)
  - [10.- Condicional `If`, `If-Else`, `Else If`, Ifs anidados](#10--condicional-if-if-else-else-if-ifs-anidados)
    - [10.1.- `if` simple](#101--if-simple)
    - [10.2.- `if-else`](#102--if-else)
    - [10.3.- `else if` (múltiples condiciones)](#103--else-if-múltiples-condiciones)
    - [10.4.- Ifs anidados](#104--ifs-anidados)
    - [10.5.- Expresiones lógicas en `if`](#105--expresiones-lógicas-en-if)
    - [10.6.- `if` sin paréntesis (solo en C# 9 con expresiones lambda o patrones)](#106--if-sin-paréntesis-solo-en-c-9-con-expresiones-lambda-o-patrones)
    - [10.7.- Operador ternario (`? :`) como alternativa a `if-else`](#107--operador-ternario---como-alternativa-a-if-else)
    - [10.8.- Optimización de `if` en C](#108--optimización-de-if-en-c)
    - [10.9.- Resumen de variantes de `if`](#109--resumen-de-variantes-de-if)
    - [10.10.- Operador ternario (`?:`)](#1010--operador-ternario-)
    - [10.11.- Pattern Matching (`is` y `switch`)](#1011--pattern-matching-is-y-switch)
      - [10.11.1.- `is` con pattern matching](#10111--is-con-pattern-matching)
      - [10.11.2.- Pattern Matching con `switch`](#10112--pattern-matching-con-switch)
      - [🔹10.11.3.- Ventajas del pattern matching](#10113--ventajas-del-pattern-matching)
  - [11.- Switch en C](#11--switch-en-c)
    - [11.1.- Sintaxis básica del switch](#111--sintaxis-básica-del-switch)
    - [11.2.- Switch sin `break` (fall-through explícito)](#112--switch-sin-break-fall-through-explícito)
    - [11.3.- Switch con múltiples tipos de valores](#113--switch-con-múltiples-tipos-de-valores)
    - [11.4.- Switch con expresiones (C# 8+)](#114--switch-con-expresiones-c-8)
    - [11.5.- Switch con patrones (Pattern Matching)](#115--switch-con-patrones-pattern-matching)
    - [11.6.- Switch con tuplas](#116--switch-con-tuplas)
    - [11.7.- Switch con enums](#117--switch-con-enums)
    - [11.8.- Optimización de switches](#118--optimización-de-switches)
    - [11.9.- Consejos y buenas prácticas](#119--consejos-y-buenas-prácticas)
    - [11.10.- Resumen de variantes de switch](#1110--resumen-de-variantes-de-switch)
  - [12.-🧩 Diferencia entre *Tupla* y *Enum* en C](#12--diferencia-entre-tupla-y-enum-en-c)
    - [🧱 1. ENUM — *Tipo de dato definido por el programador*](#-1-enum--tipo-de-dato-definido-por-el-programador)
      - [Ejemplo de ENUM](#ejemplo-de-enum)
      - [✳️ Características de ENUM](#️-características-de-enum)
    - [🧮 2. TUPLA — *Estructura de datos que agrupa valores distintos*](#-2-tupla--estructura-de-datos-que-agrupa-valores-distintos)
      - [Ejemplo de tupla](#ejemplo-de-tupla)
      - [✳️ Características de Tupla](#️-características-de-tupla)
    - [⚖️ Comparación directa](#️-comparación-directa)
  - [13.- Ciclo `for` en C](#13--ciclo-for-en-c)
    - [13.0 Introducción](#130-introducción)
    - [🔹 13.1 Estructura básica del `for`](#-131-estructura-básica-del-for)
      - [🧩 Ejemplo simple](#-ejemplo-simple)
    - [🔹 13.2 Partes del `for` explicadas](#-132-partes-del-for-explicadas)
    - [🔹 13.3 Tipos y variaciones del `for`](#-133-tipos-y-variaciones-del-for)
      - [1️⃣ For clásico (más usado)](#1️⃣-for-clásico-más-usado)
      - [2️⃣ For decreciente](#2️⃣-for-decreciente)
      - [3️⃣ For con paso personalizado](#3️⃣-for-con-paso-personalizado)
      - [4️⃣ For sin cuerpo](#4️⃣-for-sin-cuerpo)
      - [5️⃣ For infinito (cuidado ⚠️)](#5️⃣-for-infinito-cuidado-️)
    - [🔹 13.4 Variantes más modernas](#-134-variantes-más-modernas)
      - [🔸 13.4.1 For con múltiples variables](#-1341-for-con-múltiples-variables)
      - [🔸 13.4.2 For con listas o colecciones (cuando no quieres usar foreach)](#-1342-for-con-listas-o-colecciones-cuando-no-quieres-usar-foreach)
    - [🔹 13.5 Optimización del `for`](#-135-optimización-del-for)
      - [🧠 1️⃣ Evita recalcular longitudes en cada iteración](#-1️⃣-evita-recalcular-longitudes-en-cada-iteración)
      - [🧠 2️⃣ Prefiere `foreach` si solo necesitas recorrer una colección](#-2️⃣-prefiere-foreach-si-solo-necesitas-recorrer-una-colección)
      - [🧠 3️⃣ Evita operaciones costosas dentro del ciclo](#-3️⃣-evita-operaciones-costosas-dentro-del-ciclo)
      - [🧠 4️⃣ Usa paralelismo si el ciclo es muy pesado](#-4️⃣-usa-paralelismo-si-el-ciclo-es-muy-pesado)
    - [🔹 13.6 Combinando `for` con condiciones](#-136-combinando-for-con-condiciones)
    - [🔹 13.7 Uso de `break` y `continue`](#-137-uso-de-break-y-continue)
      - [🔸 `break`](#-break)
      - [🔸 `continue`](#-continue)
    - [🔹 13.8 For anidado](#-138-for-anidado)
    - [🔹 13.9 Ejemplo práctico — Tabla de multiplicar](#-139-ejemplo-práctico--tabla-de-multiplicar)
    - [🔹 13.10 Buenas prácticas para usar `for`](#-1310-buenas-prácticas-para-usar-for)
    - [🧩 13.11 Mini resumen final](#-1311-mini-resumen-final)
  - [14.- Ciclo `foreach`](#14--ciclo-foreach)
    - [🧱 Declaración básica](#-declaración-básica)
    - [🧩 Cómo funciona internamente](#-cómo-funciona-internamente)
    - [🧮 Tipos de colecciones compatibles](#-tipos-de-colecciones-compatibles)
    - [📚 Ejemplo con diccionarios](#-ejemplo-con-diccionarios)
    - [🧠 Inmutabilidad del elemento](#-inmutabilidad-del-elemento)
    - [⚡ Optimización y buenas prácticas](#-optimización-y-buenas-prácticas)
    - [🧩 `foreach` con índice (truco)](#-foreach-con-índice-truco)
    - [🔄 Variantes y equivalentes](#-variantes-y-equivalentes)
    - [🚀 Ejemplo de `await foreach` (C# 8+)](#-ejemplo-de-await-foreach-c-8)
    - [🧭 Resumen](#-resumen)
  - [15.- Ciclos `while` y `do while`](#15--ciclos-while-y-do-while)
    - [🧱 Ciclo `while` – Estructura básica](#-ciclo-while--estructura-básica)
    - [🧩 Ciclo `do while` – Estructura básica](#-ciclo-do-while--estructura-básica)
    - [🔄 Comparación rápida](#-comparación-rápida)
    - [⚙️ Ejemplo práctico: menú interactivo](#️-ejemplo-práctico-menú-interactivo)
    - [⚡ Consejos y buenas prácticas](#-consejos-y-buenas-prácticas)
    - [🧮 Optimización de ciclos `while`](#-optimización-de-ciclos-while)
    - [💡 Uso con `break` y `continue`](#-uso-con-break-y-continue)
    - [🧠 `while` infinito controlado (bucles de servicio)](#-while-infinito-controlado-bucles-de-servicio)
    - [🧩 Resumen general](#-resumen-general)
    - [🚀 Conclusión](#-conclusión)
  - [16.- Control de Flujo: `break`, `continue` y `goto`](#16--control-de-flujo-break-continue-y-goto)
    - [🧩 1️⃣ `break` — Rompe el ciclo actual](#-1️⃣-break--rompe-el-ciclo-actual)
      - [🔹 Ejemplo básico](#-ejemplo-básico)
      - [🔹 Uso en `while` y `foreach`](#-uso-en-while-y-foreach)
      - [⚙️ Casos de uso comunes](#️-casos-de-uso-comunes)
    - [🧩 2️⃣ `continue` — Salta a la siguiente iteración](#-2️⃣-continue--salta-a-la-siguiente-iteración)
      - [🔹 Ejemplo básico de `continue`](#-ejemplo-básico-de-continue)
      - [🔹 Ejemplo práctico con `while`](#-ejemplo-práctico-con-while)
      - [⚙️ Usos típicos](#️-usos-típicos)
    - [🧩 3️⃣ `goto` — Salto directo a una etiqueta](#-3️⃣-goto--salto-directo-a-una-etiqueta)
      - [🔹 Sintaxis básica](#-sintaxis-básica)
      - [🔹 Ejemplo práctico](#-ejemplo-práctico)
      - [⚠️ Cuándo (y cuándo NO) usar `goto`](#️-cuándo-y-cuándo-no-usar-goto)
      - [🔹 Ejemplo: romper varios bucles anidados](#-ejemplo-romper-varios-bucles-anidados)
    - [⚡ Resumen general](#-resumen-general-1)
    - [🧠 Optimización y buenas prácticas](#-optimización-y-buenas-prácticas-1)
      - [💡 **Ejemplo avanzado: combinación de control**](#-ejemplo-avanzado-combinación-de-control)
      - [🧩 **Conclusión**](#-conclusión-1)
  - [🧮 17.- Matrices en C# (Arrays)](#-17--matrices-en-c-arrays)
    - [🔹 17.1.- Declaración y creación de matrices](#-171--declaración-y-creación-de-matrices)
    - [🔹 17.2.- Acceso y modificación de elementos](#-172--acceso-y-modificación-de-elementos)
    - [🔹 17.3.- Recorrer matrices con `for` y `foreach`](#-173--recorrer-matrices-con-for-y-foreach)
    - [🔹 17.4.- Matrices multidimensionales](#-174--matrices-multidimensionales)
      - [Ejemplo de matriz bidimensional (como una tabla)](#ejemplo-de-matriz-bidimensional-como-una-tabla)
    - [🔹 17.5.- Matrices irregulares (Jagged Arrays)](#-175--matrices-irregulares-jagged-arrays)
    - [🔹 17.6.- Métodos útiles de la clase `Array`](#-176--métodos-útiles-de-la-clase-array)
    - [🔹 17.7.- Copiar y clonar matrices](#-177--copiar-y-clonar-matrices)
    - [🔹 17.8.- Uso avanzado: inicialización dinámica](#-178--uso-avanzado-inicialización-dinámica)
    - [🔹 17.9.- Buenas prácticas con arrays](#-179--buenas-prácticas-con-arrays)
    - [🔹 17.10.- Ejemplo completo](#-1710--ejemplo-completo)
    - [🧠 Resumen del tema](#-resumen-del-tema)
    - [🔹 17.11.- Tipos de Arreglos y Variantes Avanzadas](#-1711--tipos-de-arreglos-y-variantes-avanzadas)
      - [🧩 1. Arreglos Multidimensionales (`[,]`)](#-1-arreglos-multidimensionales-)
      - [🪜 2. Arreglos Jagged (`[][]`)](#-2-arreglos-jagged-)
      - [🔄 3. Arreglos Dinámicos (`List<T>`)](#-3-arreglos-dinámicos-listt)
      - [⚡ 4. Conversión entre Arrays y Listas](#-4-conversión-entre-arrays-y-listas)
      - [🧠 5. Redimensionar Arrays Manualmente](#-5-redimensionar-arrays-manualmente)
      - [🔍 6. Arreglos con Tipos Personalizados](#-6-arreglos-con-tipos-personalizados)
      - [⚙️ 7. Tips de Optimización](#️-7-tips-de-optimización)
  - [🧱 18.- Listas y Colecciones en C](#-18--listas-y-colecciones-en-c)
    - [🧩 18.1.- Introducción a las Colecciones Genéricas](#-181--introducción-a-las-colecciones-genéricas)
    - [📋 18.2.- List — Listas Dinámicas](#-182--list--listas-dinámicas)
    - [🔑 18.3.- Dictionary\<TKey, TValue\> — Diccionarios (Mapas Clave-Valor)](#-183--dictionarytkey-tvalue--diccionarios-mapas-clave-valor)
    - [📦 18.4.- Queue — Colas (FIFO)](#-184--queue--colas-fifo)
    - [🪃 18.5.- Stack — Pilas (LIFO)](#-185--stack--pilas-lifo)
    - [🔍 18.6.- HashSet — Conjuntos sin duplicados](#-186--hashset--conjuntos-sin-duplicados)
    - [🧮 18.7.- SortedList y SortedDictionary](#-187--sortedlist-y-sorteddictionary)
    - [🧠 18.8.- Consejos y Buenas Prácticas](#-188--consejos-y-buenas-prácticas)
    - [💡 18.9.- Ejemplo Práctico: Gestión de Estudiantes](#-189--ejemplo-práctico-gestión-de-estudiantes)
  - [🧩 19.- Métodos en C](#-19--métodos-en-c)
    - [19.1 ¿Qué es un Método?](#191-qué-es-un-método)
    - [19.2 Estructura de un Método](#192-estructura-de-un-método)
    - [19.3 Métodos `void` (sin retorno)](#193-métodos-void-sin-retorno)
    - [19.4 Métodos con Retorno](#194-métodos-con-retorno)
    - [19.5 Parámetros y Argumentos](#195-parámetros-y-argumentos)
    - [19.6 Parámetros por Valor y por Referencia](#196-parámetros-por-valor-y-por-referencia)
      - [🔹 Por Valor (default)](#-por-valor-default)
      - [🔹 Por Referencia (`ref`)](#-por-referencia-ref)
      - [🔹 Solo salida (`out`)](#-solo-salida-out)
    - [19.7 Parámetros Opcionales y con Nombre](#197-parámetros-opcionales-y-con-nombre)
    - [19.8 Métodos Estáticos (`static`)](#198-métodos-estáticos-static)
    - [19.9 Sobrecarga de Métodos (Overloading)](#199-sobrecarga-de-métodos-overloading)
    - [19.10 Expresiones Lambda (Métodos en una línea)](#1910-expresiones-lambda-métodos-en-una-línea)
    - [19.11 Métodos Locales (anidados dentro de otro método)](#1911-métodos-locales-anidados-dentro-de-otro-método)
    - [19.12 Métodos Asíncronos (`async` / `await`)](#1912-métodos-asíncronos-async--await)
    - [19.13 Buenas Prácticas](#1913-buenas-prácticas)
    - [19.14 Ejemplo Final: Calculadora Modular](#1914-ejemplo-final-calculadora-modular)
  - [🧩 20.- Métodos y Funciones Avanzadas](#-20--métodos-y-funciones-avanzadas)
    - [20.1 Recursividad](#201-recursividad)
    - [20.2 Funciones Anónimas (Anonymous Functions)](#202-funciones-anónimas-anonymous-functions)
    - [20.3 Expresiones Lambda Avanzadas](#203-expresiones-lambda-avanzadas)
    - [20.4 Delegados (Delegates)](#204-delegados-delegates)
    - [20.5 Eventos (basados en Delegados)](#205-eventos-basados-en-delegados)
    - [20.6 Métodos Genéricos](#206-métodos-genéricos)
    - [20.7 Parámetros `params`](#207-parámetros-params)
    - [20.8 Métodos de Extensión](#208-métodos-de-extensión)
    - [20.9 Métodos Asíncronos Avanzados](#209-métodos-asíncronos-avanzados)
    - [20.10 Buenas Prácticas](#2010-buenas-prácticas)
    - [20.11 Ejemplo Integrado: Calculadora Genérica y Asíncrona](#2011-ejemplo-integrado-calculadora-genérica-y-asíncrona)
  - [21.- Delegados, Eventos y LINQ en C#\*\*](#21--delegados-eventos-y-linq-en-c)
    - [21.1 ¿Qué es un Delegado?](#211-qué-es-un-delegado)
      - [Ejemplo Básico](#ejemplo-básico)
    - [21.2 Delegados Multicast](#212-delegados-multicast)
    - [21.3 Eventos](#213-eventos)
      - [Ejemplo Básico de Eventos](#ejemplo-básico-de-eventos)
    - [21.4 Delegados Genéricos (`Func` y `Action`)](#214-delegados-genéricos-func-y-action)
    - [21.5 LINQ (Language Integrated Query)](#215-linq-language-integrated-query)
      - [Ejemplo básico](#ejemplo-básico-1)
    - [21.6 Operadores LINQ Comunes](#216-operadores-linq-comunes)
      - [Ejemplo usando varios](#ejemplo-usando-varios)
    - [21.7 Buenas Prácticas para Delegados, Eventos y LINQ](#217-buenas-prácticas-para-delegados-eventos-y-linq)
  - [22.- Programación Orientada a Objetos (POO) en C](#22--programación-orientada-a-objetos-poo-en-c)
    - [22.1 Conceptos Clave](#221-conceptos-clave)
    - [22.2 Clases y Objetos](#222-clases-y-objetos)
      - [22.2.1 Declaración de una Clase](#2221-declaración-de-una-clase)
      - [22.2.2 Crear un Objeto](#2222-crear-un-objeto)
    - [22.3 Constructores](#223-constructores)
    - [22.4 Propiedades y Encapsulamiento](#224-propiedades-y-encapsulamiento)
    - [22.5 Métodos](#225-métodos)
    - [22.6 Herencia](#226-herencia)
    - [22.7 Polimorfismo](#227-polimorfismo)
    - [22.8 Abstracción](#228-abstracción)
    - [22.9 Interfaces](#229-interfaces)
    - [22.10 Buenas Prácticas en POO](#2210-buenas-prácticas-en-poo)
  - [Indice](#indice)
