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

### 🧱 **Declaración básica**

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

### 🧩 **Cómo funciona internamente**

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

### 🧮 **Tipos de colecciones compatibles**

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

### 📚 **Ejemplo con diccionarios**

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

### 🧠 **Inmutabilidad del elemento**

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

### ⚡ **Optimización y buenas prácticas**

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

### 🧩 **`foreach` con índice (truco)**

Aunque `foreach` no tiene índice directamente, puedes usar `Select` de LINQ:

```csharp
var frutas = new[] { "Manzana", "Pera", "Uva" };

foreach (var (fruta, i) in frutas.Select((valor, indice) => (valor, indice)))
{
    Console.WriteLine($"Fruta {i}: {fruta}");
}
```

---

### 🔄 **Variantes y equivalentes**

| Variante           | Descripción                                        | Ejemplo                             |
| ------------------ | -------------------------------------------------- | ----------------------------------- |
| `foreach` normal   | Itera sobre colección                              | `foreach (var x in lista)`          |
| `Parallel.ForEach` | Ejecuta iteraciones en paralelo (multi-hilo)       | `Parallel.ForEach(lista, x => ...)` |
| `await foreach`    | Itera sobre flujos asíncronos (`IAsyncEnumerable`) | `await foreach (var item in flujo)` |

---

### 🚀 **Ejemplo de `await foreach` (C# 8+)**

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

### 🧭 **Resumen**

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

### 🧱 **Ciclo `while` – Estructura básica**

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

### 🧩 **Ciclo `do while` – Estructura básica**

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

### 🔄 **Comparación rápida**

| Característica                   | `while`       | `do while`      |
| -------------------------------- | ------------- | --------------- |
| Evalúa antes de ejecutar         | ✅             | ❌               |
| Evalúa después de ejecutar       | ❌             | ✅               |
| Se puede ejecutar cero veces     | ✅             | ❌               |
| Siempre ejecuta al menos una vez | ❌             | ✅               |
| Uso típico                       | Validar antes | Validar después |

---

### ⚙️ **Ejemplo práctico: menú interactivo**

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

### ⚡ **Consejos y buenas prácticas**

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

### 🧮 **Optimización de ciclos `while`**

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

### 💡 **Uso con `break` y `continue`**

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

### 🧠 **`while` infinito controlado (bucles de servicio)**

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

### 🧩 **Resumen general**

| Tipo de ciclo | Cuándo se evalúa | Puede no ejecutarse | Ideal para...                          |
| ------------- | ---------------- | ------------------- | -------------------------------------- |
| `for`         | Antes            | ✅                   | Iteraciones contadas                   |
| `foreach`     | Automático       | ✅                   | Recorrer colecciones                   |
| `while`       | Antes            | ✅                   | Condiciones dinámicas                  |
| `do while`    | Después          | ❌                   | Ejecución garantizada al menos una vez |

---

### 🚀 **Conclusión**

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

### 🧩 **1️⃣ `break` — Rompe el ciclo actual**

Sirve para **salir inmediatamente** del ciclo (o `switch`) en el que se encuentra.
No se ejecuta el resto del bloque ni se sigue iterando.

---

#### 🔹 **Ejemplo básico**

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

#### 🔹 **Uso en `while` y `foreach`**

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

#### ⚙️ **Casos de uso comunes**

- Finalizar un ciclo al cumplir una condición.
- Salir de un menú interactivo.
- Romper una búsqueda al encontrar un resultado.

---

### 🧩 **2️⃣ `continue` — Salta a la siguiente iteración**

Omite el resto del código dentro del bloque y **pasa directamente a la siguiente iteración** del ciclo.

---

#### 🔹 **Ejemplo básico de `continue`**

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

#### 🔹 **Ejemplo práctico con `while`**

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

#### ⚙️ **Usos típicos**

- Saltar iteraciones que no cumplen un criterio.
- Evitar anidar demasiados `if` dentro de los bucles.
- Mejorar la legibilidad de condiciones complejas.

---

### 🧩 **3️⃣ `goto` — Salto directo a una etiqueta**

El temido (y mal comprendido) **`goto`** permite **saltar a una etiqueta específica del código**.
Su uso se considera **poco recomendado**, porque puede romper la estructura lógica del programa y volverlo difícil de mantener.

---

#### 🔹 **Sintaxis básica**

```csharp
goto etiqueta;

// ...
etiqueta:
Console.WriteLine("Salto completado.");
```

---

#### 🔹 **Ejemplo práctico**

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

#### ⚠️ **Cuándo (y cuándo NO) usar `goto`**

**✅ Casos válidos:**

- Para salir de varios ciclos anidados de una sola vez.
- En código muy bajo nivel o control de errores críticos (poco común en C# moderno).

**❌ Evítalo cuando:**

- Se puede resolver con `break`, `continue` o funciones separadas.
- Hace el código más difícil de leer.

---

#### 🔹 **Ejemplo: romper varios bucles anidados**

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

### ⚡ **Resumen general**

| Palabra clave | Función                          | Rompe el ciclo | Salta iteración | Salta a otro punto |
| ------------- | -------------------------------- | -------------- | --------------- | ------------------ |
| `break`       | Sale del ciclo o `switch` actual | ✅              | ❌               | ❌                  |
| `continue`    | Salta a la siguiente iteración   | ❌              | ✅               | ❌                  |
| `goto`        | Salta a una etiqueta específica  | ✅              | ❌               | ✅                  |

---

### 🧠 **Optimización y buenas prácticas**

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

## 17.-

## 18.-

## 19.-

## 20.-

## 21.-

## 22.-

## 23.-

## 24.-

## 25.-

## 26.-

## 27.-

## 28.-
