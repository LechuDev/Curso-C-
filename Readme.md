# Curso de Programación en C #

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
