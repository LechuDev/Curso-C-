# Curso de Unity básico

## Introducción

Esta es una recopilación de notas generadas a mano y con IA.
Estas notas fueron tomadas de un curso de programación de YouTube.

Solo que la información fue actualizada al 2026

Agradezco de antemano al creador de este video

[Introducción a Unity con C# - Paso a paso // Curso Completo](https://www.youtube.com/watch?v=eKjTdbf-XE4)

Y cualquier persona es libre de Explorar esta información la cual es bastante, asi que dejo a continuación link a el indice, este se abre con

'Ctrl + Click'

Acceso al indice => [Indice](#indice)

## 1. Qué es Unity

Unity es un **motor de desarrollo de videojuegos** (o _game engine_) que permite crear videojuegos y experiencias interactivas en 2D, 3D, realidad virtual (VR), realidad aumentada (AR) y más.

Algunas características clave:

* **Multiplataforma:** Puedes crear juegos para PC, consolas, móviles y web, sin tener que reescribir el código desde cero.
* **Editor visual:** Permite ver y manipular tus objetos, escenas y componentes en tiempo real.
* **Programación flexible:** Utiliza principalmente C# para controlar la lógica del juego.
* **Comunidad y recursos:** Cuenta con un vasto ecosistema de tutoriales, plugins y assets en la Asset Store.

En pocas palabras: Unity es la herramienta que conecta tus ideas con un juego que otros pueden jugar, combinando programación, gráficos y física en un solo lugar.

* * *

## 2. Qué es Unity Hub

Unity Hub es una **aplicación de administración** para Unity. No es el motor en sí, sino la forma más fácil de:

* **Instalar distintas versiones de Unity** sin conflictos.
* **Crear y abrir proyectos** rápidamente.
* **Gestionar licencias y cuentas** de Unity.
* **Agregar módulos de soporte** como Android, iOS o WebGL según la plataforma de destino.

Piensa en Unity Hub como tu “panel de control” para Unity. Desde aquí puedes iniciar cualquier proyecto y mantener todo organizado.

* * *

## 3. Instalación de Unity

Aquí te explico el proceso paso a paso:

1. **Descargar Unity Hub:**
    * Ve a la página oficial: <https://unity.com/download>
    * Descarga la versión de Unity Hub compatible con tu sistema operativo (Windows o macOS).
2. **Instalar Unity Hub:**
    * Ejecuta el instalador y sigue las instrucciones.
    * Una vez instalado, abre Unity Hub y crea o inicia sesión con tu cuenta de Unity.
3. **Instalar Unity Editor desde Unity Hub:**
    * Dentro de Unity Hub, ve a la pestaña **Installs (Instalaciones)**.
    * Haz clic en **Add (Agregar)** y selecciona la versión de Unity que deseas instalar.
    * Selecciona los **módulos adicionales** que necesites, como soporte para Android, iOS, Windows, etc.
    * Espera a que se descargue e instale.
4. **Crear un proyecto:**
    * Desde Unity Hub, ve a **Projects (Proyectos)** → **New (Nuevo)**.
    * Elige el tipo de plantilla (2D, 3D, URP, HDRP) según tu necesidad.
    * Ponle un nombre y ubicación, y presiona **Create**.

¡Listo! Ya tienes Unity instalado y un proyecto listo para comenzar a trabajar.

* * *

## 4. Diferencias entre versiones de Unity

Unity se actualiza constantemente y cada versión tiene cambios importantes. Aquí están las diferencias principales:

1. **LTS (Long Term Support – Soporte a Largo Plazo):**
    * Versión estable y confiable para proyectos grandes o profesionales.
    * Recibe solo correcciones de errores y parches de seguridad, no nuevas funciones.
    * Ideal para cuando quieres **evitar problemas de compatibilidad**.
2. **Tech Stream (Últimas funciones):**
    * Incluye las **nuevas características** de Unity.
    * Más adecuada para aprender y experimentar, pero puede tener errores o cambios frecuentes.
    * Ideal para quienes quieren explorar **lo último en gráficos, físicas y herramientas**.
3. **Compatibilidad de proyectos:**
    * Un proyecto creado en una versión más nueva de Unity puede **no abrirse correctamente** en una versión más antigua.
    * Siempre es recomendable elegir la versión que se mantendrá durante todo el desarrollo del proyecto.

* * *

## 5. Plataformas para las que puede compilar Unity

Unity es un motor **multiplataforma**, lo que significa que puedes crear un proyecto una sola vez y luego exportarlo a distintas plataformas sin reescribir todo desde cero. Entre las principales plataformas están:

1. **PC y Mac:**
    * Windows, macOS y Linux.
    * Ideal para juegos de escritorio y aplicaciones.
2. **Consolas:**
    * PlayStation, Xbox, Nintendo Switch.
    * Requiere **licencias específicas** y kits de desarrollo (SDK) de cada consola.
3. **Móviles:**
    * Android y iOS.
    * Permite integrar sensores del dispositivo como giroscopio, cámara y GPS.
4. **Web:**
    * WebGL: juegos que se ejecutan directamente en el navegador sin instalar nada.
5. **Realidad Virtual y Aumentada:**
    * VR: Oculus, HTC Vive, Valve Index.
    * AR: ARKit (iOS), ARCore (Android), HoloLens.
6. **Otras plataformas especiales:**
    * Smart TVs, dispositivos IoT, e incluso sistemas de realidad mixta.

En Unity Hub, cuando instalas el Editor, puedes **agregar módulos de soporte** para cada plataforma que quieras usar. Esto asegura que al exportar tu proyecto, Unity tenga todos los recursos necesarios.

* * *

## 6. Build y estructuras básicas de proyectos en Unity

Cuando hablamos de “Build” en Unity, nos referimos al **proceso de exportar tu juego** a una plataforma específica, generando los archivos finales que los jugadores usarán. Pero antes de eso, es importante entender cómo está estructurado un proyecto de Unity:

### 1\. Plantillas de proyecto (Project Templates)

Unity ofrece **proyectos preconfigurados** que te permiten empezar a desarrollar sin configurar todo desde cero. Estas son algunas de las plantillas más comunes:

* **3D:**
  * Para juegos o aplicaciones en tres dimensiones.
  * Incluye una escena básica con una cámara y una luz.
* **2D:**
  * Para juegos de vista superior o lateral (plataformas, puzzles, etc.).
  * La cámara y la física están configuradas para 2D.
* **URP (Universal Render Pipeline):**
  * Pipeline moderno de renderizado, eficiente para múltiples plataformas.
  * Ideal si quieres gráficos más avanzados y personalizables.
* **HDRP (High Definition Render Pipeline):**
  * Para gráficos de alta calidad en PC y consolas potentes.
  * Incluye efectos visuales avanzados como iluminación global y reflexiones realistas.
* **3D con Plantilla de Entrada:**
  * Viene con el sistema de Input preconfigurado para mover un personaje y controlar la cámara.
* **Plantillas de realidad virtual o aumentada:**
  * Configuradas para VR/AR con controladores y cámaras especiales.

Estas plantillas te permiten **enfocarte en tu juego** en lugar de configurar desde cero la iluminación, cámaras, físicas y controles básicos.

* * *

### 2\. Estructura básica de un proyecto de Unity

Dentro de un proyecto, hay carpetas y elementos importantes:

* **Assets:**
  * Todo lo que usas en tu juego (modelos 3D, sprites, sonidos, scripts, escenas).
* **Scenes (Escenas):**
  * Una “escena” es un nivel o una parte del juego.
  * Cada proyecto puede tener varias escenas (menú principal, niveles, etc.).
* **Scripts:**
  * Archivos de código en C# que controlan la lógica del juego.
* **Project Settings:**
  * Configuraciones globales del proyecto: calidad gráfica, controles, físicas, etc.
* **Packages:**
  * Módulos adicionales que Unity usa para mejorar el proyecto, como TextMeshPro (fuentes avanzadas) o Cinemachine (cámaras avanzadas).

Cuando creas un proyecto con una **plantilla**, Unity configura estas carpetas y algunas escenas básicas para que tengas un punto de partida sólido.

* * *

* * *

## 7. Cómo crear un proyecto 3D en Unity

### **Paso 1: Abrir Unity Hub**

1. Inicia **Unity Hub** desde tu escritorio o menú de inicio.
2. Asegúrate de haber iniciado sesión con tu cuenta de Unity.
3. En la ventana principal verás varias pestañas: **Projects (Proyectos)**, **Installs (Instalaciones)**, **Learn (Aprender)** y **Community (Comunidad)**.

* * *

### **Paso 2: Seleccionar la opción para crear un nuevo proyecto**

1. Ve a la pestaña **Projects**.
2. Haz clic en **New Project (Nuevo proyecto)** o el botón “New” que suele estar arriba a la derecha.

* * *

### **Paso 3: Elegir la plantilla del proyecto**

1. Se abrirá una ventana para seleccionar **plantilla (Template)**.
2. Para un proyecto 3D, elige **3D**.
    * Esta plantilla ya tiene configurada la cámara principal y la iluminación básica para un entorno 3D.
3. Opcionalmente, puedes elegir **3D URP** si quieres usar el renderizado moderno y más eficiente en gráficos.

* * *

### **Paso 4: Configurar el nombre y ubicación**

1. **Project Name (Nombre del proyecto):** escribe un nombre claro, por ejemplo: `MiPrimerJuego3D`.
2. **Location (Ubicación):** selecciona la carpeta en tu computadora donde quieres guardar tu proyecto.
3. **Organization (Organización):** si tienes una organización registrada en Unity, selecciona aquí; si no, déjalo en tu cuenta personal.

* * *

### **Paso 5: Crear el proyecto**

1. Haz clic en **Create (Crear)**.
2. Unity comenzará a preparar el proyecto; esto puede tardar unos segundos o minutos dependiendo de tu computadora y los módulos instalados.
3. Cuando termine, se abrirá automáticamente el **Editor de Unity** con tu nuevo proyecto 3D listo para trabajar.

* * *

### **Paso 6: Familiarizarse con la interfaz**

Al abrir el proyecto, verás varias áreas importantes:

1. **Scene (Escena):** espacio donde colocas y manipulas los objetos 3D.
2. **Hierarchy (Jerarquía):** lista de todos los objetos que están en la escena.
3. **Inspector:** muestra las propiedades del objeto seleccionado, como posición, rotación, escala, materiales, scripts.
4. **Project:** aquí están todos los archivos del proyecto (Assets, escenas, scripts, etc.).
5. **Game (Juego):** vista de cómo se verá tu juego cuando se ejecute.

* * *

## 8. Entradas en Unity

### 8.1 🧠 ¿Qué es el Input Manager?

El **Input Manager** es una herramienta de Unity que permite definir y gestionar los ejes de entrada (como movimiento horizontal, vertical, saltos, etc.) y sus correspondientes acciones.

* * *

#### ⚙️ ¿Cómo acceder al Input Manager?

Para acceder al Input Manager:

1. Ve al menú superior de Unity.
2. Selecciona **Edit > Project Settings**.
3. En la ventana que se abre, selecciona **Input Manager** en la lista de la izquierda.

* * *

#### 🛠️ Estructura del Input Manager

Dentro del Input Manager, encontrarás una lista de "Axes" (ejes) que representan las entradas definidas. Cada eje tiene propiedades como:

* **Name**: Nombre del eje (por ejemplo, "Horizontal").
* **Positive Button**: Tecla o botón que activa el movimiento positivo (por ejemplo, "right" o "d").
* **Negative Button**: Tecla o botón que activa el movimiento negativo (por ejemplo, "left" o "a").
* **Alt Positive Button**: Tecla alternativa para el movimiento positivo.
* **Alt Negative Button**: Tecla alternativa para el movimiento negativo.
* **Gravity**: Tiempo que tarda en detenerse la entrada cuando se deja de presionar la tecla.
* **Dead**: Umbral mínimo para que la entrada sea considerada activa.
* **Sensitivity**: Sensibilidad de la entrada.

* * *

#### 🎮 ¿Para qué se utiliza?

El Input Manager es ideal para:

* Juegos 2D y 3D sencillos.
* Prototipos rápidos.
* Proyectos que no requieren soporte avanzado para múltiples dispositivos.

* * *

#### ⚠️ Consideraciones

Aunque el Input Manager es útil, Unity ha introducido un sistema más moderno y flexible llamado **Input System**. Este nuevo sistema ofrece:

* Soporte nativo para múltiples dispositivos.
* Mapeo de controles más intuitivo.
* Mejor rendimiento y flexibilidad.

Para proyectos nuevos o más complejos, se recomienda considerar el uso del **Input System** en lugar del Input Manager tradicional.

* * *

### 8.2 🧠 ¿Qué es el Input System?

El **Input System** es un sistema avanzado de Unity para gestionar entradas de usuario, reemplazando al antiguo Input Manager. Permite:

* Soporte nativo para múltiples dispositivos (teclado, ratón, gamepads, pantallas táctiles, etc.).
* Configuración visual e intuitiva de acciones y bindings.
* Rebindeo en tiempo de ejecución.
* Soporte para múltiples esquemas de control y entradas por jugador.
* Integración con otras herramientas de Unity, como UI Toolkit y Cinemachine.

* * *

#### ⚙️ ¿Cómo instalarlo?

1. **Abrir el Package Manager**: En Unity, ve a `Window > Package Manager`.
2. **Buscar el paquete**: En el menú desplegable, selecciona "Unity Registry" y busca "Input System".
3. **Instalar**: Haz clic en "Install" para agregarlo a tu proyecto.

> **Nota**: Al instalarlo, Unity te pedirá reiniciar el editor para completar la integración.

* * *

#### 🧩 Conceptos clave

* **Input Actions**: Representan las acciones del jugador, como "Saltar", "Mover", "Disparar". Son independientes del dispositivo.
* **Bindings**: Asocian una acción a un control específico, como una tecla o botón.
* **Action Maps**: Agrupan acciones relacionadas, facilitando su gestión.
* **Player Input**: Componente que facilita la asignación de entradas a un jugador, ideal para juegos locales.

* * *

#### 🎮 Flujo básico de uso

1. **Crear un Asset de Input Actions**:
    * Haz clic derecho en el panel de Proyecto y selecciona `Create > Input Actions`.
    * Asigna un nombre, por ejemplo, `PlayerControls`.
2. **Configurar Actions**:
    * Haz doble clic en el asset creado para abrir el editor visual.
    * Añade un nuevo Action Map, por ejemplo, `Player`.
    * Dentro de este, crea acciones como `Move`, `Jump`, `Fire`.
3. **Asignar Bindings**:
    * Para cada acción, añade bindings correspondientes, como:
        * `Move`: WASD o flechas.
        * `Jump`: Barra espaciadora.
        * `Fire`: Botón izquierdo del ratón.
4. **Implementar en el código**:
    * Crea un script, por ejemplo, `PlayerController`.
    * Declara una instancia de `PlayerControls` y sus acciones.
    * En el método `OnEnable`, habilita las acciones; en `OnDisable`, deshabilítalas.
    * En el método `Update`, lee las entradas y aplica la lógica del juego.

* * *

#### 🛠️ Características avanzadas

* **Rebindeo en tiempo de ejecución**: Permite a los jugadores reasignar controles durante el juego.
* **Soporte para múltiples jugadores**: Gestiona entradas de varios jugadores simultáneamente.
* **Interacciones y procesadores**: Añade efectos como clics dobles, mantención de botones, zonas muertas, etc.
* **Integración con UI Toolkit**: Facilita la creación de interfaces de usuario interactivas.

* * *

### 8.3 1️⃣ Uso básico del Input Manager (clásico) explicado línea por línea

```csharp
using UnityEngine; // Importa el espacio de nombres de Unity, necesario para usar componentes, funciones de física y objetos del juego.

public class PlayerControllerOld : MonoBehaviour
{
    public float speed = 5f;       // Velocidad de movimiento del personaje
    public float jumpForce = 5f;   // Fuerza con la que saltará el personaje
    private Rigidbody rb;          // Referencia al Rigidbody para controlar la física

    void Start()
    {
        rb = GetComponent<Rigidbody>(); // Busca automáticamente el Rigidbody del objeto en la escena
    }

    void Update()
    {
        // Obtener el valor de los ejes de movimiento definidos en Input Manager
        float moveX = Input.GetAxis("Horizontal"); // Devuelve un valor entre -1 y 1 según la tecla presionada (A/D o flechas)
        float moveZ = Input.GetAxis("Vertical");   // Devuelve un valor entre -1 y 1 según la tecla presionada (W/S o flechas)

        // Crear un vector de movimiento en 3D basado en las entradas
        Vector3 movement = new Vector3(moveX, 0, moveZ) * speed * Time.deltaTime;

        // Mover el personaje en el mundo (Space.World evita que se mueva relativo a la rotación del objeto)
        transform.Translate(movement, Space.World);

        // Detectar si se presiona el botón de salto (por defecto es "Jump", normalmente la barra espaciadora)
        if (Input.GetButtonDown("Jump"))
        {
            // Aplicar fuerza hacia arriba para saltar
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
        }
    }
}
```

✅ **Notas clave:**

* `Input.GetAxis()` es gradual: permite movimiento suave (aceleración/desaceleración).
* `Input.GetButtonDown()` se dispara **solo una vez** cuando se presiona la tecla.
* El sistema clásico está limitado a los dispositivos definidos en Input Manager.

* * *

### 8.4 2️⃣ Uso básico del Input System (moderno) explicado línea por línea

```csharp
using UnityEngine;              // Importa funcionalidades de Unity
using UnityEngine.InputSystem;  // Importa el Input System moderno

public class PlayerControllerNew : MonoBehaviour
{
    public float speed = 5f;        // Velocidad de movimiento
    public float jumpForce = 5f;    // Fuerza del salto
    private Rigidbody rb;           // Referencia al Rigidbody
    private PlayerControls controls; // Instancia del asset Input Actions
    private Vector2 moveInput;       // Almacena la entrada de movimiento como Vector2 (x = horizontal, y = vertical)

    void Awake()
    {
        rb = GetComponent<Rigidbody>();        // Captura el Rigidbody del objeto
        controls = new PlayerControls();       // Crea la instancia del asset Input Actions (archivo PlayerControls.inputactions)

        // Registrar callback para la acción Move cuando se realiza
        controls.Player.Move.performed += ctx => moveInput = ctx.ReadValue<Vector2>();
        // Cuando se cancela el movimiento (se suelta la tecla o joystick), se pone el vector a cero
        controls.Player.Move.canceled += ctx => moveInput = Vector2.zero;

        // Registrar callback para la acción Jump cuando se realiza
        controls.Player.Jump.performed += ctx => Jump();
    }

    void OnEnable()
    {
        controls.Enable();  // Habilita el asset de Input Actions para que comience a leer entradas
    }

    void OnDisable()
    {
        controls.Disable(); // Deshabilita el asset para evitar que siga leyendo entradas cuando el objeto está inactivo
    }

    void Update()
    {
        // Crear vector de movimiento en 3D a partir del Vector2 recibido
        Vector3 movement = new Vector3(moveInput.x, 0, moveInput.y) * speed * Time.deltaTime;
        // Mover el personaje en el mundo
        transform.Translate(movement, Space.World);
    }

    void Jump()
    {
        // Aplicar fuerza hacia arriba para saltar
        rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
    }
}
```

✅ **Notas clave:**

* `ctx.ReadValue<Vector2>()` lee la entrada actual de un eje o stick (teclado o gamepad).
* `performed` se activa cuando la acción ocurre, `canceled` cuando se deja de presionar.
* Funciona con múltiples dispositivos sin cambiar el código.
* Permite **rebindeo dinámico** y manejo de **múltiples jugadores** fácilmente.

* * *

### 8.5 💡 **Resumen comparativo rápido**

| Característica | Input Manager | Input System |
| --- | --- | --- |
| Dispositivos | Limitados (teclado, joystick básico) | Todos (teclado, mouse, gamepad, VR, touch) |
| Flexibilidad | Baja | Alta |
| Rebindeo dinámico | No | Sí |
| Facilidad de prototipos | Alta | Media |
| Recomendado para | Proyectos simples | Proyectos nuevos/avanzados |

* * *

## 9. Assets, GameObjects y Componentes

### **1️⃣ Qué son los Assets**

En Unity, un **Asset** es cualquier recurso que utilizas en tu proyecto.  
Piensa en los Assets como **materiales o herramientas** que tu juego necesita para existir.

**Ejemplos de Assets:**

* Modelos 3D (.fbx, .obj)
* Imágenes o sprites (.png, .jpg)
* Texturas y materiales
* Sonidos y música (.wav, .mp3)
* Animaciones
* Scripts en C#
* Prefabs (objetos preconfigurados que incluyen GameObjects y componentes)

**Características clave:**

* Se almacenan en la carpeta **Assets** dentro del proyecto.
* Pueden ser creados por ti, importados de la **Asset Store** o generados dentro de Unity.
* No tienen presencia directa en la escena hasta que los agregas como GameObjects.

**Ejemplo práctico:**  
Si importas un modelo 3D de un cubo, ese modelo es un Asset. Luego lo arrastras a la escena para usarlo como objeto.

* * *

### **2️⃣ Qué son los GameObjects**

Un **GameObject** es un **objeto dentro de la escena**.  
Todo lo que aparece en tu juego es un GameObject: un jugador, un enemigo, un árbol, una luz, la cámara, incluso partículas de polvo.

**Características clave:**

* Puede estar vacío o contener Assets y Componentes.
* Es el **contenedor básico** de Unity para organizar todo en la escena.
* Puede tener **jerarquía**: un GameObject puede ser “padre” de otros (“hijos”).

**Ejemplo:**

```text
GameObject "Player"
 ├─ GameObject "Cuerpo"
 ├─ GameObject "Cabeza"
 └─ GameObject "Arma"
```

Aquí, el jugador es un GameObject principal y tiene otros GameObjects como hijos.

* * *

### **3️⃣ Qué son los Componentes**

Los **Componentes** son **funcionalidades que se agregan a los GameObjects**.  
Un GameObject por sí solo no hace nada; los componentes le dan comportamiento, apariencia y física.

**Ejemplos de Componentes comunes:**

* **Transform:** Posición, rotación y escala del objeto (todos los GameObjects lo tienen por defecto).
* **Mesh Renderer:** Permite que el objeto sea visible en 3D.
* **Rigidbody:** Añade física al objeto (gravedad, colisiones).
* **Collider:** Detecta colisiones con otros objetos.
* **Script:** Código personalizado que define comportamiento (por ejemplo, mover al jugador).

**Ejemplo práctico:**  
Si tienes un GameObject llamado “Pelota”:

* Le agregas un **Rigidbody** → puede caer y rebotar.
* Le agregas un **Sphere Collider** → detecta colisiones con el suelo o paredes.
* Le agregas un **Script de control** → el jugador puede lanzarla o moverla.

En Unity, todo se basa en esta **estructura: GameObject + Componentes + Assets**.

* * *

💡 **Analogía rápida:**

* **Asset:** La materia prima o recurso (como madera, pintura o sonido).
* **GameObject:** La caja o contenedor donde construyes algo (como una figura de madera).
* **Componente:** Las partes o herramientas que le das al objeto para que funcione (como ruedas, motor, pegamento, pintura).

* * *

## 10. **1️⃣ Qué es una cámara en Unity**

En Unity, una **cámara (Camera)** es un componente que define **desde dónde y cómo se ve el mundo del juego**.  
Sin una cámara, aunque tengas objetos y escenas, el jugador **no verá nada**.

**Características clave:**

* Captura la escena y la proyecta en la pantalla.
* Controla perspectiva, campo de visión, profundidad y efectos de postprocesado.
* Cada escena puede tener una o varias cámaras, pero normalmente solo una principal activa para renderizar.

* * *

### **2️⃣ Tipos de cámaras**

Unity tiene un solo tipo de componente cámara, pero se pueden configurar de varias formas:

1. **Perspective (Perspectiva):**
    * La más común en juegos 3D.
    * Los objetos más lejanos se ven más pequeños, igual que en la vida real.
    * Ideal para juegos de acción, aventura, carreras, FPS/3D.
2. **Orthographic (Ortográfica):**
    * No hay perspectiva: todos los objetos se ven del mismo tamaño sin importar la distancia.
    * Ideal para juegos 2D, estrategia, simulación o isométricos.
3. **Cinemachine Camera (opcional, paquete):**
    * Sistema avanzado para manejar cámaras dinámicas.
    * Permite seguimiento de personajes, cámaras con suavizado, transiciones y efectos cinemáticos.
    * No reemplaza la cámara normal, sino que se combina con ella.

* * *

### **3️⃣ Para qué se usan**

Las cámaras son esenciales para:

* **Renderizar el juego**: mostrar al jugador lo que sucede.
* **Crear efectos visuales**: profundidad de campo, desenfoque, zoom, perspectiva.
* **Controlar la vista del jugador**: seguir al personaje, cambiar ángulos, escenas cinematográficas.
* **Cinemáticas y menús**: mostrar escenas específicas, minimapas o cámaras de UI.

* * *

### **4️⃣ Cómo se crean y configuran**

### **Crear una cámara nueva**

1. Ve al menú superior: `GameObject > Camera > Camera`.
2. Unity crea un GameObject con el componente **Camera** ya agregado.

### **Configurar sus propiedades principales**

* **Clear Flags:** define qué se dibuja detrás (Skybox, Solid Color, Depth Only, Nothing).
* **Background:** color de fondo si no usas Skybox.
* **Culling Mask:** qué capas de objetos verá la cámara.
* **Projection:** Perspective u Orthographic.
* **Field of View (FOV):** ángulo de visión (solo para Perspective).
* **Orthographic Size:** tamaño de visión (solo para Orthographic).
* **Depth:** orden en que la cámara renderiza respecto a otras cámaras.

### **Hacer que la cámara siga un objeto**

1. Crear un script, por ejemplo, `CameraFollow`.
2. Asociar la cámara al personaje.

```csharp
using UnityEngine;

public class CameraFollow : MonoBehaviour
{
    public Transform target; // Objeto a seguir
    public Vector3 offset;   // Distancia relativa entre la cámara y el objeto

    void LateUpdate()
    {
        if(target != null)
        {
            // Actualiza la posición de la cámara respecto al objetivo
            transform.position = target.position + offset;
            // Mantiene la cámara mirando al objetivo
            transform.LookAt(target);
        }
    }
}
```

✅ **Notas:**

* `LateUpdate()` se usa para que la cámara se mueva después de que el personaje se haya actualizado.
* `offset` permite separar la cámara del jugador (por ejemplo, detrás y arriba).

* * *

💡 **Consejo práctico para novatos:**

* Siempre ten una cámara principal (`Main Camera`) activa en tu escena.
* Para juegos 2D, usa Orthographic; para 3D, Perspective.
* Cinemachine es muy útil cuando quieras cámaras suaves y dinámicas sin programar demasiado.

* * *

## 11. **2️⃣🎥 **¿Qué es Cinemachine?**

**Cinemachine** es un sistema de cámaras inteligente que te permite:

* Crear cámaras que **siguen a personajes** automáticamente.
* Hacer **transiciones suaves** entre cámaras.
* Controlar **ángulos, zoom, enfoque y movimiento** sin código.
* Crear **escenas cinemáticas**, cámaras fijas, cámaras tipo “tercera persona”, “primera persona” o “Top-Down”.

En pocas palabras:  
💡 **Cinemachine es como tener un camarógrafo profesional dentro de Unity.**

* * *

### 🧩 **Cómo instalar Cinemachine**

1. Abre Unity Hub y entra a tu proyecto.
2. En el menú superior, ve a **Window → Package Manager**.
3. En la lista de paquetes, busca **Cinemachine**.
4. Haz clic en **Install**.
5. Listo, ahora tendrás una nueva opción en el menú:  
    `GameObject → Cinemachine`.

* * *

### ⚙️ **Cómo crear una cámara Cinemachine básica**

#### 📍 Paso 1: Crear una cámara virtual

* Ve a: **GameObject → Cinemachine → Create Virtual Camera**.
* Se creará un objeto llamado algo como `CM vcam1`.

> 🧠 Las **Virtual Cameras** no son cámaras reales; son configuraciones que controlan a la **Main Camera**.  
> La cámara principal del juego sigue las órdenes de la Virtual Camera activa.

* * *

#### 📍 Paso 2: Asignar un objetivo (Follow y Look At)

Selecciona la Virtual Camera y verás esto en el **Inspector**:

* **Follow:** el objeto que la cámara debe seguir (por ejemplo, tu jugador).
* **Look At:** el objeto al que la cámara debe mirar (también puede ser el jugador o parte del cuerpo).

Ejemplo:  
Arrastra tu objeto `Player` a ambos campos y verás cómo la cámara lo sigue automáticamente. 🎮

* * *

#### 📍 Paso 3: Ajustar el comportamiento de la cámara

En el mismo panel del **Inspector**:

* **Body:** controla el movimiento físico de la cámara.
  * 🌀 _Transposer_ → movimiento en tercera persona.
  * 📸 _Framing Transposer_ → cámara más cinematográfica.
  * 🚁 _Orbital Transposer_ → cámara que puede rotar alrededor del objetivo.
* **Aim:** controla hacia dónde mira la cámara.
  * 🎯 _Hard Look At_ → siempre mira directamente al objetivo.
  * 🔭 _Composer_ → te permite ajustar el encuadre (por ejemplo, mantener al jugador en el tercio inferior de la pantalla).

* * *

### 🎬 **Tipos de cámaras Cinemachine más usados**

| Tipo de Cámara | Descripción | Ideal para |
| --- | --- | --- |
| 🎥 **Virtual Camera** | Cámara base, se usa para seguir al jugador o una escena. | Cualquier tipo de juego. |
| 🚁 **FreeLook Camera** | Cámara orbital que sigue y rota alrededor del personaje. | Juegos en tercera persona tipo GTA o Fortnite. |
| 👁️ **ClearShot Camera** | Cambia automáticamente entre cámaras según la mejor vista. | Escenas con obstáculos o cámaras inteligentes. |
| 🎞️ **Blend List Camera** | Secuencia de cámaras para cinemáticas o intros. | Escenas narrativas. |
| 🕹️ **State-Driven Camera** | Cambia entre cámaras según animaciones o estados del personaje. | Juegos con múltiples modos (correr, saltar, etc.). |

* * *

### 🧠 **Ejemplo básico con FreeLook Camera**

Supongamos que quieres una cámara tipo “tercera persona”:

1. Crea un objeto:  
    `GameObject → Cinemachine → FreeLook Camera`.
2. Asigna tu jugador a los campos **Follow** y **Look At**.
3. Ajusta las “Orbit Rigs” (Top Rig, Middle Rig, Bottom Rig).
    * Esto define cómo la cámara orbita alrededor del jugador.
4. ¡Pulsa Play y prueba con el ratón o joystick!  
    La cámara se moverá suavemente alrededor del personaje.

* * *

### 💻 **Cinemachine en código (uso opcional)**

Aunque Cinemachine casi no necesita código, puedes controlarla desde scripts:

```csharp
using UnityEngine;
using Cinemachine;

public class CameraManager : MonoBehaviour
{
    public CinemachineVirtualCamera virtualCamera;

    void Start()
    {
        // Cambiar campo de visión dinámicamente
        virtualCamera.m_Lens.FieldOfView = 70f;
    }

    public void Zoom(float zoomLevel)
    {
        // Zoom suave (reducir campo de visión)
        virtualCamera.m_Lens.FieldOfView = Mathf.Lerp(
            virtualCamera.m_Lens.FieldOfView,
            zoomLevel,
            Time.deltaTime * 2f
        );
    }
}
```

📝 _En este ejemplo, puedes controlar el zoom o cambiar propiedades de la cámara durante el juego._

* * *

### 🎨 **Ventajas de usar Cinemachine**

✅ Movimiento y seguimiento **suaves** sin código.  
✅ Control preciso de encuadres y transiciones.  
✅ Compatible con **Timeline** para cinemáticas.  
✅ Perfecto para cámaras complejas o multijugador.  
✅ Fácil de ajustar visualmente en el **Editor**.

* * *

### 💡 **Consejos profesionales**

* Usa **FreeLook Camera** para juegos 3D de personaje.
* Usa **2D Virtual Camera** para plataformas.
* Combina **Cinemachine + Timeline** para escenas tipo película.
* Puedes usar varias Virtual Cameras y **cambiar entre ellas con transiciones suaves** automáticamente.

* * *

## 12. ☀️ **1️⃣ Qué son las luces en Unity**

En Unity, las **luces (Lights)** son **componentes** que simulan la iluminación del mundo real dentro del motor gráfico.  
Afectan cómo se ven los colores, las sombras, los reflejos y la profundidad de los objetos en tu escena.

📌 En resumen:

> Las luces determinan **cómo se ven tus modelos 3D** y **cómo se siente la atmósfera del juego** (fría, cálida, tenebrosa, futurista, etc.).

* * *

### 💡 **2️⃣ Tipos de luces en Unity**-

Unity tiene **cuatro tipos principales de luces**, y cada una se usa para propósitos distintos:

| Tipo de luz | Descripción | Uso común |
| --- | --- | --- |
| ☀️ **Directional Light** | Ilumina toda la escena desde una dirección infinita (como el sol). | Luz del día o sol. |
| 💡 **Point Light** | Emite luz en todas direcciones desde un punto. | Lámparas, bombillos, fuego, antorchas. |
| 🔦 **Spot Light** | Emite un cono de luz direccional (como una linterna o foco). | Linternas, reflectores, faros. |
| 🕶️ **Area Light** _(solo en modo baked)_ | Emite luz desde una superficie rectangular. | Luces de interiores o neones (solo en renderizado estático). |

* * *

### 🛠️ **3️⃣ Cómo crear una luz**

### 📍 Método 1 – Desde el menú

1. Ve a la barra superior → `GameObject > Light`.
2. Elige el tipo: **Directional, Point, Spot o Area**.
3. Aparecerá un nuevo GameObject con el componente **Light**.

### 📍 Método 2 – Desde la jerarquía

1. Clic derecho en el panel **Hierarchy**.
2. `Light → Tipo de luz que quieras crear`.

* * *

### ⚙️ **4️⃣ Propiedades principales del componente Light**

Cuando seleccionas una luz, verás en el **Inspector** algo como esto:

| Propiedad | Descripción |
| --- | --- |
| **Type** | Tipo de luz (Directional, Point, Spot, Area). |
| **Color** | Color de la luz (puedes dar tonos cálidos, fríos, etc.). |
| **Intensity** | Qué tan fuerte o brillante es la luz. |
| **Range** | Distancia hasta donde llega (solo Point y Spot). |
| **Spot Angle** | Apertura del cono de luz (solo Spot). |
| **Shadows** | Tipo de sombras (None, Hard, Soft). |
| **Cookie** | Máscara para proyectar patrones de sombra (rejillas, persianas, etc.). |

* * *

### 🌞 **5️⃣ Tipos de sombras**

Las luces pueden proyectar **sombras**, lo cual añade profundidad y realismo.

* **No Shadows:** sin sombras (más rápido, pero menos realista).
* **Hard Shadows:** sombras con bordes definidos.
* **Soft Shadows:** sombras difusas y suaves (más realistas, pero consumen más rendimiento).

💡 _Consejo:_ usa **Soft Shadows** solo cuando sea necesario, ya que afectan el rendimiento.

* * *

### 🔥 **6️⃣ Modos de iluminación: Real-Time, Mixed y Baked**

Unity ofrece tres formas de procesar la luz:

| Modo | Descripción | Ideal para |
| --- | --- | --- |
| **Realtime** | Se calcula en tiempo real (cambia mientras el juego corre). | Linternas, luces dinámicas, efectos. |
| **Baked** | Se calcula antes del juego y se guarda en “texturas de luz” (lightmaps). | Escenarios estáticos (paredes, pisos). |
| **Mixed** | Combina ambos: la iluminación estática se hornea, pero los objetos dinámicos reaccionan. | Escenarios semi-estáticos. |

🎯 **Ejemplo:**  
Una habitación iluminada por focos fijos → _Baked_.  
El jugador con una linterna → _Realtime_.  
Un fuego que cambia de intensidad → _Mixed_.

* * *

### 💻 **7️⃣ Ejemplo simple de luz dinámica con código**

Vamos a hacer que una luz parpadee como una antorcha 🔥:

```csharp
using UnityEngine;

public class FlickeringLight : MonoBehaviour
{
    private Light lightSource;
    public float minIntensity = 0.8f;
    public float maxIntensity = 1.2f;

    void Start()
    {
        // Obtenemos el componente de luz
        lightSource = GetComponent<Light>();
    }

    void Update()
    {
        // Cambiamos aleatoriamente la intensidad
        lightSource.intensity = Random.Range(minIntensity, maxIntensity);
    }
}
```

📘 **Explicación:**

* `Light lightSource` → guardamos la luz.
* `Random.Range()` → genera un valor aleatorio entre dos límites.
* En cada frame (`Update()`), cambiamos la intensidad → parpadeo natural.

🎮 Así se simula una antorcha, fuego o luz defectuosa.

* * *

### 🌗 **8️⃣ Luces y rendimiento**

⚠️ **Importante:**  
Cada luz **Realtime** consume rendimiento, especialmente si proyecta sombras.

**Consejos para optimizar:**

* Usa **Baked Lights** en escenarios estáticos.
* Usa **Realtime Lights** solo para objetos que se muevan.
* Ajusta el **Range** de las Point y Spot Lights para que no iluminen áreas innecesarias.
* Desactiva las luces que el jugador no ve (con `SetActive(false)` o distancia de cámara).

* * *

### ✨ **9️⃣ Efectos y postprocesado**

Puedes mejorar el look general con **Post Processing**:

* Bloom (efecto de brillo suave).
* Color Grading (temperatura del color).
* Ambient Occlusion (profundidad en sombras).
* Vignette (oscurece los bordes de la pantalla).

Esto hace que tus luces resalten y tu juego luzca más profesional.

* * *

### 💡 **1️⃣0️⃣ Consejos finales**

✅ Usa **Directional Light** para el sol o la luna.  
✅ Usa **Point Light** para fuentes pequeñas como velas.  
✅ Usa **Spot Light** para linternas o faros.  
✅ Mezcla luces cálidas y frías para dar realismo.  
✅ Activa **Global Illumination** para rebote de luz realista.

* * *

## 13. 🎬 **1️⃣ Qué es una Scene (Escena)**

En Unity, una **Scene** es un **espacio de trabajo o entorno completo** que contiene todos los **GameObjects** que componen un momento o parte de tu juego.

> 💡 Piensa en cada _Scene_ como un “capítulo” del juego:
>
> * Una Scene puede ser el menú principal.
> * Otra puede ser el primer nivel.
> * Otra puede ser una cinemática o un escenario especial.

* * *

### 🧩 **2️⃣ Qué contiene una Scene**

Cada Scene puede tener:

* **GameObjects** (jugadores, enemigos, luces, cámaras, etc.)
* **Terrenos** o entornos 3D
* **UI** (interfaces gráficas, botones, menús)
* **Luces y efectos**
* **Scripts** que controlan el comportamiento
* **Datos específicos del nivel** (música, configuraciones, triggers)

📘 En resumen:

> Una Scene es como un **mundo independiente dentro del juego**, con sus propios objetos, scripts y configuraciones.

* * *

### 🏗️ **3️⃣ Dónde se guardan las Scenes**

Por defecto, Unity crea una carpeta llamada **`Assets/Scenes/`**.  
Dentro de ella encontrarás un archivo como:

```yaml
SampleScene.unity
```

Cada archivo `.unity` representa una escena.

👉 Puedes tener **tantas escenas como quieras** en tu proyecto.

* * *

### ⚙️ **4️⃣ Cómo crear una nueva Scene**

#### 📍 Opción 1 – Desde el menú

1. `File → New Scene`
2. Elige la plantilla (2D, 3D, URP, HDRP, etc.)
3. Guarda la escena con `File → Save As…`
4. Colócala en la carpeta `Assets/Scenes/` con un nombre claro.  
    Ejemplo: `Nivel1.unity` o `MenuPrincipal.unity`.

#### 📍 Opción 2 – Desde la jerarquía

* Clic derecho en la carpeta `Scenes` → `Create → Scene`.

* * *

### 🧠 **5️⃣ Cómo abrir y cambiar de Scene**

* Para abrir una escena manualmente, haz doble clic en ella desde el **Project Window**.
* Para cambiar de escena _durante el juego_, se usa el **SceneManager** (requiere importar `using UnityEngine.SceneManagement`).

📜 Ejemplo básico:

```csharp
using UnityEngine;
using UnityEngine.SceneManagement;

public class CambiarEscena : MonoBehaviour
{
    public void IrAEscena(string nombreEscena)
    {
        // Carga una escena nueva por nombre
        SceneManager.LoadScene(nombreEscena);
    }
}
```

🧩 **Ejemplo de uso:**

```csharp
IrAEscena("Nivel2");
```

👉 Esto reemplazará la escena actual por la llamada “Nivel2”.

* * *

### 🔄 **6️⃣ Tipos de carga de escenas**

Unity permite diferentes modos de carga:

| Método | Descripción | Ejemplo |
| --- | --- | --- |
| `LoadScene("Nivel2")` | Reemplaza completamente la escena actual. | Cambio de nivel. |
| `LoadScene("UI", LoadSceneMode.Additive)` | Carga otra escena **sin cerrar la actual**. | HUD, menús o transiciones. |
| `UnloadSceneAsync("UI")` | Descarga una escena previamente añadida. | Cerrar panel o menú temporal. |

💡 _Additive_ se usa mucho para **dividir escenarios grandes** o **modularizar el proyecto**.

* * *

### 🧱 **7️⃣ Escena activa y administración**

Unity siempre tiene una **Scene activa** (la principal).  
Puedes cambiarla por código:

```csharp
SceneManager.SetActiveScene(SceneManager.GetSceneByName("Nivel1"));
```

Esto es útil cuando trabajas con varias escenas cargadas al mismo tiempo (por ejemplo, “Mapa + UI”).

* * *

### 🌍 **8️⃣ Scene View vs Game View**

| Vista | Descripción |
| --- | --- |
| **Scene View** | Es el entorno de edición. Puedes mover objetos, cambiar luces, probar posiciones, etc. No afecta el juego en sí. |
| **Game View** | Es lo que el jugador verá cuando se ejecute el juego. Está controlado por la cámara principal. |

💡 Consejo: usa el **gizmo de cámara** en la esquina superior derecha para moverte fácilmente en la Scene View.

* * *

### 🔦 **9️⃣ Ejemplo: crear una escena completa desde cero**

1. Crea una nueva Scene y llámala `Nivel1`.
2. Agrega:
    * Un **Directional Light** (sol).
    * Una **Main Camera**.
    * Un **Plano** (Ground).
    * Un **Cubo** (Player).
3. Guarda la escena (`Ctrl + S`).

🎮 Si le das Play, ya tienes un mini nivel funcional.

* * *

### 💾 **🔟 Cómo agregar escenas al Build Settings**

Para que una escena pueda usarse al compilar o cargarse desde código:

1. Ve a: `File → Build Settings`.
2. Clic en **Add Open Scenes** (añade la actual).
3. Repite con todas las escenas que usarás.

El orden en la lista define el **índice de escena**, útil si cargas por número:

```csharp
SceneManager.LoadScene(1);
```

* * *

### ⚡ **1️⃣1️⃣ Buenas prácticas**

✅ Usa nombres claros: `MenuPrincipal`, `Nivel1_Bosque`, `Nivel2_Ciudad`.  
✅ Agrupa escenas por tipo: `Scenes/Game`, `Scenes/UI`, `Scenes/Cinematics`.  
✅ Guarda la escena antes de darle Play (evita perder cambios).  
✅ Usa `DontDestroyOnLoad()` para mantener objetos persistentes (como música o datos del jugador).  
✅ Aprovecha la carga _additiva_ para dividir grandes mundos en zonas.

* * *

### 🧙‍♂️ **1️⃣2️⃣ Ejemplo de sistema de transición entre escenas con animación**

```csharp
using UnityEngine;
using UnityEngine.SceneManagement;

public class TransicionEscena : MonoBehaviour
{
    public Animator transicion;
    public float tiempoTransicion = 1f;

    public void CargarSiguienteEscena(string nombreEscena)
    {
        StartCoroutine(Cargar(nombreEscena));
    }

    IEnumerator Cargar(string nombreEscena)
    {
        // Activa la animación de transición (por ejemplo, un fade-out)
        transicion.SetTrigger("Start");

        // Espera un segundo antes de cambiar de escena
        yield return new WaitForSeconds(tiempoTransicion);

        SceneManager.LoadScene(nombreEscena);
    }
}
```

🎨 Así puedes tener transiciones suaves entre niveles (pantallas negras, fundidos, etc.).

* * *

### 🎮 **1️⃣3️⃣Controles para moverte en la Escena (Scene View)**

Cuando trabajas en Unity, la **Scene View** es tu ventana para moverte por el mundo 3D. Aquí puedes **rotar, moverte, acercarte, alejarte y seleccionar objetos**.  
Los controles se parecen bastante a los de un videojuego en primera persona o a los de software de modelado 3D.

* * *

#### 🧭 Movimiento básico del punto de vista

| Acción | Tecla o combinación | Descripción |
| --- | --- | --- |
| **Rotar la vista** | Mantén **botón derecho del ratón** | Gira la cámara libremente (como un FPS). |
| **Moverse (trasladar la vista)** | Con el **botón derecho** presionado + teclas **W, A, S, D, Q, E** | Te mueves adelante, atrás, izquierda, derecha, arriba, abajo. _(Como moverte en un juego en primera persona)_ |
| **Desplazamiento lateral (pan)** | Mantén **botón central (rueda)** o **Alt + clic medio** | Mueve la vista en el plano sin rotarla. |
| **Orbit (girar alrededor de un objeto)** | Mantén **Alt + clic izquierdo** | Rota la cámara alrededor del objeto seleccionado. |
| **Zoom** | Rueda del ratón o **Alt + clic derecho** | Acerca o aleja la cámara. |
| **Enfocar objeto seleccionado** | Tecla **F** | Centra y acerca la cámara al objeto seleccionado. _(Muy útil para no perderlo en el espacio 3D)_ |
| **Mover más lento o más rápido** | Mantén **Shift** para ir más rápido o **Ctrl** para ir más lento | Ajusta la velocidad del movimiento de cámara. |

* * *

#### 🧠 Consejillo pro

Si alguna vez “pierdes” tu escena y no ves nada, selecciona cualquier objeto en el **Hierarchy** y presiona **F** para que Unity te lleve directo a él.

* * *

## 14. ☀️ ¿Qué es el “Auto-Generating Lighting” en Unity?

Cuando creas una escena, Unity puede **calcular automáticamente cómo la luz rebota e ilumina los objetos**, y luego **guardar (bakear)** esos datos para que el juego corra más rápido.  
Este proceso se llama **“Baking”** o **“Lightmapping”** y el ajuste que lo controla es el famoso **Auto Generate**.

En pocas palabras:

> El Auto-Generate Lighting hace que Unity actualice automáticamente los mapas de luz (Lightmaps) cada vez que cambias algo que afecta la iluminación.

* * *

### ⚙️ ¿Dónde está la opción?

1. Abre tu escena.
2. Ve al menú superior: **Window → Rendering → Lighting**.
3. Se abrirá una ventana llamada **Lighting Settings**.
4. En la parte superior o inferior verás una casilla llamada **“Auto Generate”**.

🔘 Si está **activada**, Unity recalculará automáticamente la iluminación cada vez que muevas una luz, cambies materiales o posiciones objetos.  
🔘 Si está **desactivada**, deberás presionar el botón **“Generate Lighting”** manualmente para actualizar la luz horneada (baked).

* * *

### 💡 Tipos de iluminación que intervienen

Unity combina varios tipos de luz en su sistema de generación:

| Tipo de luz | Descripción | ¿Participa en el Bake? |
| --- | --- | --- |
| **Realtime** | Se calcula en tiempo real (ideal para luces que se mueven o cambian). | ❌ No |
| **Mixed** | Parte se calcula en tiempo real, parte se hornea. | ✅ Parcial |
| **Baked** | Se hornea completamente; no cambia durante el juego. | ✅ Sí |

👉 Las luces **Baked** son ideales para escenas estáticas (como interiores o fondos).  
👉 Las **Realtime** son para objetos o luces que cambian o se mueven (como el Sol que rota).

* * *

### 🧱 ¿Qué se genera al “Bakear” la luz?

Cuando presionas **“Generate Lighting”**, Unity crea varios elementos en tu proyecto:

1. **Lightmaps** – Texturas que guardan la información de cómo la luz ilumina los objetos.
2. **Reflection Probes** – Capturan reflejos del entorno.
3. **Ambient Occlusion (opcional)** – Sombrea áreas donde la luz casi no llega.
4. **Lighting Data Asset** – Archivo donde Unity guarda toda esa info para la escena.

* * *

### ⚡ Cuándo usar Auto Generate o hacerlo manual

| Caso | Recomendación |
| --- | --- |
| Estás **editando constantemente la escena** y moviendo luces u objetos. | ✅ Usa **Auto Generate** para ver los cambios en tiempo real. |
| Tienes una **escena grande o compleja**, y recalcular es lento. | ❌ Desactiva **Auto Generate** y haz clic manualmente en **Generate Lighting** cuando termines de ajustar todo. |
| Estás preparando la **versión final del juego** o haciendo una **build**. | ✅ Genera manualmente la luz (Bake final) para rendimiento óptimo. |

* * *

### 🌈 Consejos pro

* Usa **Light Probes** para objetos móviles en escenas con iluminación horneada.
* Ajusta la calidad del bake en **Lighting Settings → Lightmapping Settings** (puedes controlar resolución, rebotes de luz, compresión, etc.).
* Si tu escena se ve muy oscura después del bake, revisa que tus **Materiales** tengan los shaders adecuados y que los objetos tengan activada la casilla **Static → Lightmap Static**.

* * *

¿Quieres que te muestre paso a paso **cómo configurar una iluminación completa y hacer un bake de luz** (con Skybox, Directional Light, Lightmap y Reflection Probe) para una escena 3D desde cero?  
Así te quedaría como una mini guía práctica.

* * *

## 15. 🧱 ¿Qué es un Material en Unity?

Un **Material** en Unity define **cómo se ve la superficie de un objeto** cuando la luz incide sobre él.  
En otras palabras, el material le dice al motor **“cómo debe comportarse la luz”** en cada punto del objeto:  
si debe **reflejarla, absorberla, difuminarla, brillar, parecer metal, tela, plástico, etc.**

👉 Un **Mesh Renderer** (el componente que dibuja el objeto) necesita **un Material** para poder mostrarse correctamente.

* * *

### 🌈 ¿De qué está hecho un Material?

Un material es un contenedor que usa un **Shader**.  
El **Shader** es un pequeño programa que le indica a la tarjeta gráfica cómo dibujar el material.

Por ejemplo:

* Un **Shader estándar** (Standard Shader) puede simular metal, vidrio, madera o piel.
* Un **Shader HDRP o URP** tiene parámetros más avanzados (reflejos, rugosidad, translucidez, etc.).
* También puedes crear tus propios shaders con **Shader Graph**.

### Estructura básica de un Material

| Propiedad | Qué hace |
| --- | --- |
| **Albedo (Color / Textura base)** | Define el color principal o la textura del material. |
| **Metallic** | Cuánto se comporta como un metal (0 = plástico, 1 = metal pulido). |
| **Smoothness (Brillo)** | Qué tan suave o reflectante es la superficie. |
| **Normal Map** | Añade detalles en relieve sin aumentar los polígonos. |
| **Height Map / Bump Map** | Simula profundidad. |
| **Emission** | Hace que el material emita luz (ideal para neones o pantallas). |
| **Tiling & Offset** | Repite o desplaza las texturas sobre la superficie. |

* * *

### 🧩 ¿Dónde se crean y cómo se aplican?

### 🪄 Crear un nuevo Material

1. En el **Project Window**, haz clic derecho.
2. Selecciona **Create → Material**.
3. Nómbralo como quieras (ejemplo: `Metal_Puerta` o `Madera_Piso`).
4. En el **Inspector**, podrás modificar sus propiedades.

### 🎨 Aplicar un Material a un objeto

Tienes varias formas:

* Arrastra el material directamente **sobre el objeto** en la vista de escena.
* O asígnalo manualmente desde el componente **Mesh Renderer → Element 0**.
* También puedes asignarlo por código.

📘 Ejemplo en C#:

```csharp
// Asignar un material desde script
public class CambiarMaterial : MonoBehaviour
{
    public Material nuevoMaterial; // arrastra el material aquí desde el inspector

    void Start()
    {
        GetComponent<Renderer>().material = nuevoMaterial;
    }
}
```

🧠 **Explicación:**

* `GetComponent<Renderer>()` obtiene el componente visual del objeto.
* `.material` accede al material actual.
* Lo reemplazamos por `nuevoMaterial`, el que arrastramos en el Inspector.

* * *

### ⚙️ Tipos de Shaders más comunes

| Shader | Descripción | Uso típico |
| --- | --- | --- |
| **Standard Shader (Built-in)** | El más versátil. Soporta metal, plástico, transparencia, etc. | Escenas normales. |
| **URP/Lit Shader** | Optimizado para el **Universal Render Pipeline (URP)**. | Proyectos móviles o multiplataforma. |
| **HDRP/Lit Shader** | Iluminación física ultra realista. | Proyectos AAA o cinematográficos. |
| **Unlit Shader** | No recibe luz, se muestra tal cual. | Interfaces, efectos 2D, HUDs. |
| **Shader Graph Shader** | Creado visualmente mediante nodos. | Efectos personalizados, agua, fuego, etc. |

* * *

### ✨ Texturas (las "pinturas" del material)

Las **texturas** son imágenes (normalmente .png, .jpg o .tga) que se asignan a las propiedades del material.  
Ejemplo:

* Una textura de ladrillo en el **Albedo**.
* Un mapa de relieve en el **Normal Map**.
* Un mapa de rugosidad en el **Smoothness**.

Puedes conseguir texturas gratuitas en sitios como:  
🧱 **cc0textures.com**, **ambientcg.com**, **textures.com**, o **Poly Haven**.

* * *

### 🧠 Tips de uso

* Si varios objetos usan el mismo material → Unity los **agrupa** para optimizar el rendimiento.
* Si cambias un material **en tiempo de ejecución**, usa `.sharedMaterial` para no duplicarlo.
* En juegos grandes, agrupa materiales por tipo de shader para mejorar el **batching** (rendimiento).

* * *

## 16. 🧭 ¿Qué es el Componente Transform?

El **Transform** es **el corazón de todo GameObject en Unity**.  
Cada objeto en tu escena (una cámara, una luz, un cubo, un enemigo, una partícula, etc.) tiene **obligatoriamente un componente Transform** que define:

1. **Position** – Dónde está el objeto en el espacio (coordenadas X, Y, Z).
2. **Rotation** – Hacia dónde apunta o cómo está girado.
3. **Scale** – Qué tan grande o pequeño es.

* * *

### 📦 Estructura del Transform en el Inspector

Cuando seleccionas un objeto, verás su Transform en el panel **Inspector**:

| Propiedad | Ejemplo | Significado |
| --- | --- | --- |
| **Position** | (0, 1, -5) | Ubicación en el espacio 3D. |
| **Rotation** | (0, 90, 0) | Rotación en grados (ejes X, Y, Z). |
| **Scale** | (1, 1, 1) | Tamaño del objeto. 1 = tamaño original. |

📌 _Todas estas propiedades están medidas en **unidades del mundo 3D**.  
Por defecto, 1 unidad = 1 metro (aproximadamente)._

* * *

### 🌎 Coordenadas locales vs globales

El Transform maneja dos sistemas de referencia:

| Tipo de espacio | Qué significa |
| --- | --- |
| **Global (World Space)** | Las coordenadas absolutas dentro del mundo. |
| **Local (Local Space)** | Las coordenadas relativas al objeto padre. |

Ejemplo:

* Si mueves un objeto **dentro de otro (padre)**, su `Position` pasa a ser **relativa al padre**.
* Si el padre rota, el hijo también rota, aunque su `Position` local no cambie.

🎯 **Esto permite jerarquías**: mover una nave espacial mueve también sus alas, propulsores, etc.

* * *

### 🧠 ¿Cómo manipular el Transform en código?

El Transform es una propiedad pública que se accede directamente desde cualquier `MonoBehaviour`.

### 🧩 Ejemplo básico

```csharp
using UnityEngine;

public class MovimientoBasico : MonoBehaviour
{
    void Update()
    {
        // Mover el objeto 1 unidad por segundo en el eje X
        transform.Translate(Vector3.right * Time.deltaTime);

        // Rotar constantemente sobre el eje Y
        transform.Rotate(Vector3.up * 50 * Time.deltaTime);

        // Cambiar escala con el tiempo (efecto pulso)
        float scale = Mathf.PingPong(Time.time, 1) + 1;
        transform.localScale = new Vector3(scale, scale, scale);
    }
}
```

* * *

### 🔍 Explicación línea por línea

```csharp
transform.Translate(Vector3.right * Time.deltaTime);
```

➡️ Mueve el objeto **hacia la derecha** (eje X positivo).  
`Time.deltaTime` asegura que el movimiento sea **independiente del framerate** (suave y constante).

```csharp
transform.Rotate(Vector3.up * 50 * Time.deltaTime);
```

➡️ Rota el objeto sobre su eje **Y** (vertical) a **50 grados por segundo**.

```csharp
float scale = Mathf.PingPong(Time.time, 1) + 1;
transform.localScale = new Vector3(scale, scale, scale);
```

➡️ `Mathf.PingPong` genera un valor que oscila entre 0 y 1.  
Al sumarle 1, la escala varía entre 1 y 2 → crea un efecto de “respiración” o pulso.

* * *

### ⚙️ Métodos útiles del Transform

| Método o Propiedad | Qué hace |
| --- | --- |
| `transform.position` | Devuelve o establece la posición global. |
| `transform.localPosition` | Posición relativa al objeto padre. |
| `transform.rotation` | Rotación global (Quaternion). |
| `transform.localRotation` | Rotación local. |
| `transform.localScale` | Escala local. |
| `transform.forward` | Dirección “frontal” del objeto. |
| `transform.right` | Dirección derecha del objeto. |
| `transform.up` | Dirección superior del objeto. |
| `transform.LookAt(target)` | Hace que el objeto mire hacia otro punto. |
| `transform.Translate(Vector3 direction)` | Mueve el objeto. |
| `transform.Rotate(Vector3 eulerAngles)` | Rota el objeto en grados. |
| `transform.SetParent(padre)` | Asigna un nuevo objeto padre. |

* * *

### 🎮 Ejemplo práctico: seguir un objetivo

```csharp
using UnityEngine;

public class SeguirObjeto : MonoBehaviour
{
    public Transform objetivo; // Asigna en el inspector

    void Update()
    {
        // Mirar siempre al objetivo
        transform.LookAt(objetivo);

        // Seguirlo con una pequeña distancia
        transform.position = Vector3.Lerp(
            transform.position, 
            objetivo.position - transform.forward * 3f, 
            Time.deltaTime * 2
        );
    }
}
```

🧩 Explicación:

* `LookAt()` alinea el frente del objeto hacia el objetivo.
* `Vector3.Lerp()` interpola suavemente la posición actual hacia la del objetivo.
* `transform.forward * 3f` mantiene una distancia de 3 unidades detrás.

* * *

### 🧱 Jerarquías y Transform hijo/padre

Cada Transform puede tener **hijos** o **un padre**, formando una estructura jerárquica.

### Ejemplo visual

```yaml
Player (Transform)
 ┣━ Head (Transform)
 ┣━ Arm_L (Transform)
 ┗━ Arm_R (Transform)
```

Si mueves o rotas el `Player`, **todas las partes hijas se mueven con él**, manteniendo su posición relativa.

* * *

### 🧩 Manipulación avanzada (por código)

```csharp
// Acceder a hijos
Transform hijo = transform.GetChild(0);

// Contar cuántos hijos tiene
int totalHijos = transform.childCount;

// Buscar un hijo por nombre
Transform brazo = transform.Find("Arm_R");

// Convertir coordenadas locales ↔ globales
Vector3 posMundo = transform.TransformPoint(Vector3.zero);
Vector3 posLocal = transform.InverseTransformPoint(posMundo);
```

* * *

### 💡 Tips finales

* Nunca cambies directamente `rotation` con ángulos; usa `Quaternion.Euler()` para evitar errores de gimbal.
* Si necesitas movimiento físico (con colisiones), usa `Rigidbody.MovePosition()` en lugar de `transform.position`.
* `transform` está **siempre disponible**; no necesitas hacer `GetComponent<Transform>()`.

* * *

¿Quieres que te muestre ahora una **miniguía visual** sobre cómo manipular el Transform **desde el editor (con los gizmos y atajos de teclado)** y cómo funciona cada herramienta (Move, Rotate, Scale, Rect Tool, etc.)?  
Eso complementaría perfecto la parte práctica del Transform 🔧

* * *

## 17. 🧭 ¿Qué es el Inspector en Unity?

El **Inspector** es un panel que muestra **todas las propiedades y componentes del GameObject** que tienes seleccionado en la escena o en el Hierarchy.

Piensa en él como una **radiografía interactiva** de cada objeto:  
si seleccionas una cámara, verás su Transform, su configuración de cámara, sus scripts, su tag, su capa, etc.  
Si seleccionas un material, verás sus texturas, su shader y sus parámetros.

📍 **Ubicación:** normalmente está en el lado derecho de la interfaz de Unity (aunque puedes moverlo donde quieras).

* * *

### 🧱 Estructura general del Inspector

Cuando seleccionas un GameObject, el Inspector muestra:

1. **Barra superior del objeto**
    * 📛 **Nombre del objeto.**
    * 🏷️ **Tag:** para clasificar el objeto (por ejemplo, “Player”, “Enemy”, “UI”).
    * 🎯 **Layer:** define en qué capa está (importante para cámaras y colisiones).
    * ✅ **Casilla de activación:** activa/desactiva el objeto completo (`SetActive(true/false)`).
    * ⚙️ **Menú contextual:** con opciones como "Reset", "Remove Component", "Copy/Paste Component", etc.
2. **Componentes**
    * El Inspector lista todos los **Componentes** que forman al objeto, en orden.  
        Ejemplo:
        * Transform
        * Mesh Renderer
        * Box Collider
        * Scripts personalizados
3. **Botón “Add Component”**
    * Sirve para agregar nuevos componentes a ese GameObject (físicos, visuales, de script, etc.).

* * *

### 🎚️ Cómo usarlo eficientemente

### 🔍 1. Editar propiedades en tiempo real

* Puedes cambiar **valores numéricos**, **activar o desactivar componentes**, **asignar materiales o scripts**, etc.
* Los cambios se reflejan **al instante** en la vista de escena y en el juego.

### 🧩 2. Arrastrar y soltar referencias

* Puedes **arrastrar objetos desde el Hierarchy o Project** hacia campos públicos del Inspector (por ejemplo, un script con `public Transform objetivo;`).
* Así se crean las **referencias** entre objetos sin escribir código.

### 🔒 3. Bloquear el Inspector

* Usa el **candadito 🔒** (arriba a la derecha) para “fijar” la vista del Inspector.  
    Así puedes seleccionar otros objetos sin perder el foco del actual.

### ⚙️ 4. Menú de componentes

* Cada componente tiene un **engranaje ⚙️** arriba a la derecha con opciones:
  * **Reset:** vuelve el componente a sus valores por defecto.
  * **Remove Component:** lo elimina.
  * **Copy / Paste Component Values:** copia sus parámetros.
  * **Move Up / Down:** cambia el orden de los componentes.

* * *

### 🎨 Inspector en modo Play

Cuando ejecutas el juego (Play Mode), el Inspector se **actualiza en tiempo real**:

* Puedes ver valores que cambian dinámicamente (posición, velocidad, vida del jugador, etc.).
* Puedes modificarlos _mientras el juego corre_ para probar comportamientos.

⚠️ **Importante:**  
Cuando detienes el juego, los cambios hechos en Play Mode **no se guardan** (a menos que uses herramientas específicas o scripts para eso).

* * *

### 🧠 Inspector y Scripts personalizados

Cuando creas un **script en C#**, cualquier variable pública o marcada con `[SerializeField]` aparecerá automáticamente en el Inspector.

Ejemplo:

```csharp
using UnityEngine;

public class ConfigJugador : MonoBehaviour
{
    public float velocidad = 5f;
    public int vida = 100;
    [SerializeField] private string nombre = "LechuDev";
}
```

🧩 En el Inspector verás tres campos:

* `Velocidad`
* `Vida`
* `Nombre`

Puedes modificarlos sin tocar el código — Unity los serializa automáticamente.

* * *

### 🧰 Custom Inspectors (para pros)

Unity te deja crear **Inspectores personalizados** para tus scripts, usando la API del **Editor**.  
Esto te permite crear sliders, botones, secciones plegables, colores, etc.

Ejemplo básico:

```csharp
using UnityEngine;
using UnityEditor;

[CustomEditor(typeof(ConfigJugador))]
public class ConfigJugadorEditor : Editor
{
    public override void OnInspectorGUI()
    {
        // Referencia al script original
        ConfigJugador jugador = (ConfigJugador)target;

        // Campo editable de velocidad
        jugador.velocidad = EditorGUILayout.Slider("Velocidad", jugador.velocidad, 0f, 20f);

        // Botón personalizado
        if (GUILayout.Button("Restablecer vida"))
        {
            jugador.vida = 100;
        }

        // Dibuja el resto del Inspector normal
        DrawDefaultInspector();
    }
}
```

💡 Esto se guarda dentro de una carpeta llamada **Editor/**, y solo afecta al entorno de edición, no al juego en sí.

* * *

### ⚡ Atajos útiles y trucos

| Acción | Atajo / Truco |
| --- | --- |
| Duplicar componente | Click derecho → Duplicate Component |
| Cambiar varios objetos a la vez | Selecciona varios en el Hierarchy y edita sus propiedades en conjunto |
| Buscar en el Inspector | Usa la barra superior (filtro por componente) |
| Ver datos ocultos (debug) | Clic en los tres puntos del Inspector → **Debug Mode** |

* * *

### 🧩 Ejemplo de flujo completo

1. Creas un objeto vacío → `GameObject > Create Empty`.
2. En el Inspector cambias el nombre a **Player**.
3. Ajustas su **Transform** (posición, rotación, escala).
4. Agregas un **Rigidbody** y un **Box Collider** desde “Add Component”.
5. Añades un script llamado `MovimientoJugador.cs`.
6. En el Inspector cambias la **velocidad** a 8.5.
7. Arrastras un **GameObject** como referencia en un campo público del script.

Todo eso sin escribir más de 3 líneas de código. 😎

* * *

### 🎯 En resumen

| Elemento | Función |
| --- | --- |
| **Inspector** | Panel que muestra y permite editar los componentes de un objeto. |
| **Componentes** | Son los “módulos” o comportamientos del objeto. |
| **Add Component** | Añade nuevos módulos al objeto. |
| **Modo Play** | Permite probar valores dinámicamente. |
| **Scripts personalizados** | Pueden exponer variables para modificarlas sin código. |
| **Custom Inspectors** | Te permiten crear interfaces propias dentro del editor. |

* * *

## 18. 🧩 **La Consola de Unity**

### 📜 ¿Qué es la Consola?

La **Consola** (Window → General → Console) es la ventana donde Unity muestra **mensajes importantes sobre lo que está pasando en tu proyecto**.  
Aquí aparecen los **errores, advertencias, logs y mensajes de depuración** generados por el motor o por tu propio código.

Podríamos decir que es el “médico del proyecto”:  
si algo se rompe, **la consola te lo dice primero**.

* * *

### ⚙️ ¿Dónde se encuentra?

Generalmente está en la parte inferior del editor, junto a las pestañas “Project”, “Hierarchy” o “Game”.  
Si no la ves, puedes abrirla desde:

> **Menú:** `Window → General → Console`

* * *

### 💬 Tipos de Mensajes en la Consola

Unity clasifica los mensajes con íconos de colores y formas distintas:

| Tipo | Icono | Color | Descripción |
| --- | --- | --- | --- |
| **Log** | ● | Blanco | Mensajes informativos. Los usas para mostrar datos o confirmar que algo se ejecuta. |
| **Warning (Advertencia)** | ⚠️ | Amarillo | Indica posibles problemas que **no detienen el juego**, pero pueden causar errores más adelante. |
| **Error** | ❌ | Rojo | Algo ha fallado. El juego puede **no compilar o no funcionar correctamente** hasta que lo soluciones. |

* * *

### 🔢 Tipos de Errores más comunes

#### 🟥 1. **Errores de Compilación**

Son los más graves.  
Unity **no puede ejecutar el juego** mientras haya uno solo de estos.

**Ejemplo:**

```csharp
void Start()
{
    Debug.Log("Hola Mundo")
}
```

> ❌ Error: _“; expected”_ → te faltó un punto y coma al final de la línea.

* * *

#### 🟨 2. **Warnings (Advertencias)**

No detienen la ejecución, pero indican malas prácticas o código obsoleto.

**Ejemplo:**

```csharp
int vida;
Debug.Log(vida);
```

> ⚠️ Advertencia: _“Variable ‘vida’ is assigned but its value is never used”_  
> o _“Variable ‘vida’ might not have been initialized”_  
> → Significa que declaraste algo pero no lo inicializaste o usaste mal.

* * *

#### ⚪ 3. **Logs e Información**

Los usas tú mismo para depurar tu código:

```csharp
Debug.Log("Jugador ha saltado");
Debug.LogWarning("Poca vida restante");
Debug.LogError("Jugador ha muerto");
```

Cada uno se mostrará con el color correspondiente.  
Esto es **clave para testear comportamientos** sin abrir 20 Debuggers distintos.

* * *

### 🧰 Botones y Filtros de la Consola

En la parte superior verás varios íconos muy útiles:

| Botón | Función |
| --- | --- |
| **Clear (🧹)** | Limpia todos los mensajes de la consola. |
| **Collapse** | Agrupa mensajes repetidos para no saturar la lista. |
| **Clear on Play** | Borra los mensajes automáticamente cuando presionas Play. |
| **Error Pause** | Pausa la ejecución del juego **automáticamente** cuando aparece un error. Súper útil al depurar. |
| **Play/Edit Mode** | Muestra mensajes que solo ocurren durante la ejecución o en el modo edición. |
| **Search Bar 🔍** | Filtra mensajes por texto, ideal para encontrar logs específicos. |

* * *

### 🧠 Consejos Pro para Usarla Bien

1. **Activa “Clear on Play” y “Collapse”** cuando estés probando código.
2. **Lee el error completo** y haz clic en él: Unity te lleva directo a la línea del script donde ocurrió.
3. Si no entiendes un error, **copia el texto exacto y pégalo en Google/ChatGPT**.  
    9 de cada 10 veces ya alguien tuvo el mismo problema.
4. **Usa `Debug.Log()` con etiquetas claras**:

    ```csharp
    Debug.Log("[Jugador] Saltó en frame: " + Time.frameCount);
    ```

    Así sabrás de dónde viene el mensaje.
5. **Ignora los warnings del motor de Unity**, pero **no los tuyos** 😜.

* * *

### 🧩 Bonus: Depuración en Tiempo Real

En modo **Play**, puedes abrir la consola y ver los mensajes en tiempo real mientras ejecutas el juego.  
Esto te permite **rastrear comportamientos paso a paso**, por ejemplo:

```csharp
void Update()
{
    if (Input.GetKeyDown(KeyCode.Space))
        Debug.Log("Saltó en: " + Time.time);
}
```

* * *

### 🧭 En Resumen

| Concepto | Descripción |
| --- | --- |
| **Consola** | Muestra errores, advertencias y mensajes de depuración. |
| **Tipos de Mensajes** | Log (blanco), Warning (amarillo), Error (rojo). |
| **Uso Común** | Depurar, entender fallos, validar lógica. |
| **Botones Clave** | Clear, Collapse, Error Pause, Clear on Play. |
| **Pro Tip** | Usa logs personalizados y revisa el stack trace del error. |

* * *

## 19. 🧱 **La Ventana Hierarchy (Jerarquía)**

### 🧩 ¿Qué es?

La **Hierarchy** muestra **todos los objetos que existen dentro de tu escena actual**.  
Cada uno de esos elementos es un **GameObject**, con sus componentes, posición y relaciones entre sí.

Piensa en la Hierarchy como el “árbol genealógico” de tu escena.  
Aquí puedes ver _qué pertenece a qué_, quién es el _padre_ y quién es el _hijo_.

* * *

### 🧠 Ejemplo visual

Imagina una escena con un jugador y una cámara:

```yaml
Main Camera
Directional Light
Player
└── Body
    ├── Arm_R
    └── Arm_L
```

* `Player` es el **padre**.
* `Body`, `Arm_R`, `Arm_L` son **hijos** (dependen del Player).
* Si mueves el `Player`, sus hijos también se mueven con él.

Esto te permite organizar tus objetos lógicamente y evitar caos visual.

* * *

### ⚙️ Acciones básicas

| Acción | Cómo hacerlo |
| --- | --- |
| **Crear un nuevo objeto vacío** | `Ctrl + Shift + N` o clic derecho → _Create Empty_ |
| **Renombrar** | Selecciona y presiona `F2` |
| **Eliminar** | `Supr` o clic derecho → _Delete_ |
| **Duplicar** | `Ctrl + D` |
| **Arrastrar para anidar** | Arrastra un objeto sobre otro para hacerlo su hijo. |
| **Buscar objetos** | Usa la barra de búsqueda en la parte superior. |

* * *

### 🧭 Tips profesionales

* 🔒 **Usa Empty Objects** como carpetas visuales.  
    Ejemplo: un objeto vacío llamado “Environment” con todos los árboles y edificios dentro.
* 🎯 **Organiza por grupos lógicos:**  
    “Player”, “Enemies”, “Props”, “UI”, “Lights”, etc.
* 👁️ **Desactiva o activa objetos** con la casilla a la izquierda de su nombre.  
    Esto permite probar cosas sin borrarlas.
* 💡 **Doble clic** en un objeto para enfocar la cámara de escena en él.

* * *

## 20. 📦 **La Ventana Project (Proyecto)**

### 📁 ¿Qué es?

La ventana **Project** es el **explorador de archivos interno de Unity**.  
Aquí se muestra todo lo que está guardado dentro de tu carpeta `Assets/` del proyecto.

Si la _Hierarchy_ muestra lo que está “en la escena”,  
la _Project_ muestra **todo lo que existe en el proyecto**, aunque no esté en la escena.

* * *

### 🗂️ Estructura típica de carpetas

Por convención, muchos proyectos se organizan así:

```yaml
Assets/
│
├── Animations/
├── Audio/
├── Materials/
├── Models/
├── Prefabs/
├── Scenes/
├── Scripts/
└── Textures/
```

Cada una tiene su propósito:

| Carpeta | Contiene |
| --- | --- |
| **Animations** | Archivos `.anim`, controladores de animación (`AnimatorController`). |
| **Audio** | Sonidos `.mp3`, `.wav`, música, efectos. |
| **Materials** | Materiales para los modelos 3D. |
| **Models** | Modelos `.fbx`, `.obj`, `.blend`, etc. |
| **Prefabs** | Objetos configurados que puedes reutilizar. |
| **Scenes** | Las distintas escenas del juego. |
| **Scripts** | Tu código C#. |
| **Textures** | Imágenes o texturas. |

* * *

### ⚙️ Acciones útiles en el Project

| Acción | Cómo hacerlo |
| --- | --- |
| **Crear carpeta** | Clic derecho → _Create → Folder_ |
| **Crear script** | Clic derecho → _Create → C# Script_ |
| **Importar assets** | _Right Click → Import New Asset…_ o arrastrar desde el explorador de Windows. |
| **Buscar archivos** | Usa la barra de búsqueda arriba. |
| **Duplicar / Renombrar** | Igual que en la Hierarchy (`Ctrl+D`, `F2`). |
| **Ver modos** | Puedes cambiar entre modo **lista** y **iconos** (botones arriba a la derecha). |

* * *

### 🧠 Relación entre Project y Hierarchy

Esta parte es clave:

> Lo que está en la **Project Window** es un _archivo_,  
> lo que está en la **Hierarchy** es una _instancia_ de ese archivo dentro de la escena.

Por ejemplo:

* En `Project` tienes un prefab llamado **Player**.
* En `Hierarchy`, tienes **una copia (instancia)** de ese prefab que puedes mover, rotar y configurar.
* Si cambias el prefab base en `Project`, todas las instancias se actualizan automáticamente.

Esto te permite **trabajar de forma modular y escalable**.

* * *

### 🎓 Pro Tip

Puedes pensar en la relación así:

* **Project:** “la receta del pastel 🍰”.
* **Hierarchy:** “el pastel que estás horneando ahora mismo”.

* * *

### 🔎 Diferencias rápidas

| Ventana | Muestra | Contenido editable |
| --- | --- | --- |
| **Hierarchy** | Objetos activos en la escena actual | Posición, componentes, relaciones |
| **Project** | Archivos del proyecto (Assets) | Scripts, texturas, modelos, escenas |

* * *

### 🧩 En Resumen

| Concepto | Descripción |
| --- | --- |
| **Hierarchy** | Muestra todos los objetos que existen en la escena actual. |
| **Project** | Muestra todos los recursos y archivos del proyecto. |
| **Relación** | De la ventana Project arrastras objetos hacia la Hierarchy para usarlos en tu escena. |
| **Consejo** | Mantén una organización clara desde el inicio para evitar caos más adelante. |

* * *

## 🧩 **Ventanas principales de Unity**

Unity organiza su interfaz en **ventanas (Windows/Panels)** que puedes mover, anclar o desacoplar. Cada ventana tiene una función específica y, combinadas, te permiten **controlar el juego, los assets, la escena y la depuración**.

* * *

### 1️⃣ **Scene Window (Escena)**

* **Qué es:** La ventana donde construyes tu mundo 3D o 2D.
* **Para qué sirve:**
  * Mover, rotar y escalar objetos.
  * Visualizar la escena desde cualquier ángulo.
  * Colocar cámaras, luces y objetos en el espacio.
* **Herramientas de manipulación:**
  * **Move Tool (W)**: mover objetos.
  * **Rotate Tool (E)**: rotar objetos.
  * **Scale Tool (R)**: cambiar el tamaño.
  * **Rect Tool (T)**: para UI y 2D.
* **Atajos de cámara:**
  * Click derecho + mover mouse → girar la cámara.
  * Scroll → acercar/alejar.
  * Alt + Click izquierdo → orbitar alrededor de un punto.
  * F → enfocar objeto seleccionado.

* * *

### 2️⃣ **Game Window (Juego)**

* **Qué es:** Muestra cómo se verá el juego cuando se ejecute.
* **Para qué sirve:**
  * Ver la escena desde la perspectiva de la cámara principal.
  * Probar la interacción y el comportamiento del juego.
  * Ver efectos de UI y renderización final.
* **Opciones:**
  * Escoge resolución y aspecto del juego (16:9, 1080p, custom).
  * Botón **Maximize on Play**: la ventana Game ocupa todo el espacio mientras pruebas.

* * *

### 3️⃣ **Other Useful Windows (Otras ventanas útiles)**

| Ventana | Función |
| --- | --- |
| **Animator** | Controla animaciones, estados y blend trees de un objeto. |
| **Lighting** | Configuración de luces, lightmaps y ambient occlusion. |
| **Profiler** | Analiza rendimiento y uso de recursos en tiempo real. |
| **Package Manager** | Instala paquetes, assets y librerías oficiales o externas. |
| **Timeline** | Controla animaciones y cinemáticas secuenciales. |
| **Audio Mixer** | Controla y mezcla el sonido de tu juego. |

* * *

### 🔹 Organización de ventanas

* Puedes **arrastrar cualquier ventana y acoplarla** en otra.
* **Layouts predefinidos:** `Window → Layouts → Default/2 by 3/4 Split`, etc.
* **Guardar tu propio layout:** útil si trabajas siempre con 2 monitores o quieres ventanas separadas.

* * *

### 💡 Tipos de uso

1. **Edición y construcción** → Scene + Hierarchy + Inspector + Project.
2. **Pruebas y juego** → Game + Console + Inspector.
3. **Optimización y depuración** → Profiler + Console + Scene/Game.
4. **Animaciones y cinemáticas** → Animator + Timeline + Scene.

* * *

En resumen:

* **Scene Window:** donde construyes tu mundo.
* **Game Window:** cómo lo ve el jugador.
* **Inspector:** detalles de los objetos.
* **Hierarchy:** objetos de la escena.
* **Project:** todos los assets.
* **Console:** depuración.
* **Otras ventanas:** dependen de tu flujo (animación, audio, luz, rendimiento).

* * *

## 🧩 **¿Qué es un Prefab?**

Un **Prefab** es básicamente un **objeto o conjunto de objetos configurados que se guardan como plantilla** en tu proyecto.

* Puedes tener una **instancia** de ese prefab en la escena (Hierarchy).
* Puedes modificar el prefab original y **todas las instancias se actualizarán automáticamente**.
* También puedes modificar una instancia individual sin afectar al prefab base.

En otras palabras:

> Prefab = receta → Hierarchy = pastel que horneas con esa receta

* * *

### 🧱 **Ventajas de usar Prefabs**

1. **Reutilización:** crea un objeto una vez y úsalo en todas las escenas.
2. **Actualizaciones masivas:** cambiar el prefab actualiza todas sus instancias.
3. **Organización:** mantiene el proyecto limpio y estructurado.
4. **Instanciación dinámica:** puedes crear objetos durante el juego con código usando prefabs.

* * *

### ⚙️ **Cómo crear un Prefab**

1. Selecciona un **GameObject** o grupo de objetos en la **Hierarchy**.
2. Arrástralo hacia la carpeta **Project → Prefabs**.
3. Se creará un **Prefab** con un icono azul.
4. Ahora puedes borrar el objeto de la escena y **instanciarlo nuevamente** desde el Project.

* * *

### 🧠 **Tipos de Prefab en Unity 2025**

Unity ahora maneja **prefabs con jerarquía avanzada** y tres modos principales:

| Tipo | Función |
| --- | --- |
| **Prefab Regular** | Plantilla base que puedes instanciar en cualquier escena. |
| **Variant (Variante)** | Prefab derivado que hereda todas las propiedades del original pero permite modificaciones propias. Ideal para enemigos o ítems con pequeñas diferencias. |
| **Nested Prefab (Prefabs Anidados)** | Prefab dentro de otro prefab. Ej: un arma dentro de un personaje. Cambiar el arma afecta solo el prefab de arma, no el personaje. |

* * *

### 🔹 **Instanciar Prefabs por código**

```csharp
using UnityEngine;

public class Spawner : MonoBehaviour
{
    public GameObject enemigoPrefab; // Asignar prefab en el inspector
    public Transform spawnPoint;     // Lugar donde aparecerá

    void Start()
    {
        // Crear una instancia del prefab en la escena
        GameObject nuevoEnemigo = Instantiate(enemigoPrefab, spawnPoint.position, spawnPoint.rotation);

        // Opcional: cambiar nombre de la instancia
        nuevoEnemigo.name = "Enemigo_1";
    }
}
```

**Explicación línea a línea:**

* `public GameObject enemigoPrefab;` → referencia al prefab que arrastramos en el Inspector.
* `Instantiate(...)` → crea una **nueva copia en la escena** con posición y rotación definidas.
* `nuevoEnemigo.name = "Enemigo_1";` → cambia el nombre de la instancia (opcional).

💡 Esto es clave para juegos donde necesitas generar enemigos, proyectiles o ítems dinámicamente.

* * *

### 🧩 **Editar Prefabs**

* **Modo Prefab:** haz doble clic en el prefab en el Project.
  * La escena se abre en un **modo especial donde solo editas el prefab**.
  * Puedes añadir componentes, hijos, scripts o modificar Transform sin afectar otras escenas.
* **Overrides (Sobrescrituras):** si modificas una instancia en la escena, verás los cambios como sobrescrituras.
  * Puedes **aplicar al prefab** o **descartar los cambios**.

* * *

### ⚡ **Tips Profesionales**

1. **Usa prefabs para todo lo que se repita**: enemigos, puertas, efectos, UI, props.
2. **Organiza prefabs en carpetas** dentro de `Assets/Prefabs` para no perderlos.
3. **Anidar prefabs** te permite construir objetos complejos de manera modular.
4. **Variants** son útiles cuando necesitas pequeños cambios sin duplicar el prefab original.
5. **Nunca modifiques un prefab directamente en una escena si quieres mantener consistencia**; usa el modo Prefab o aplica overrides.

* * *

En resumen:

* Prefab = plantilla reusable de un GameObject.
* Se pueden instanciar en la escena cuantas veces quieras.
* Permite jerarquías y variantes.
* Fundamental para organizar proyectos grandes y para instanciar objetos dinámicamente en tiempo de ejecución.

* * *

## 🧩 **¿Qué es un Script en Unity?**

Un **Script** es un archivo de código, normalmente en **C#**, que se asocia a un GameObject mediante un componente.

* Le dice al objeto **qué hacer y cómo reaccionar**.
* Controla movimiento, interacciones, animaciones, físicas, UI, enemigos, etc.

💡 Piensa en un **Prefab** como un “cuerpo” y un **Script** como su “cerebro”.

* * *

### 🧱 **Estructura básica de un Script en Unity (C#)**

Cuando creas un script nuevo (`Create → C# Script`), Unity genera algo como esto:

```csharp
using UnityEngine;

public class MiPrimerScript : MonoBehaviour
{
    // Start se llama antes del primer frame
    void Start()
    {
        Debug.Log("Hola Mundo");
    }

    // Update se llama cada frame
    void Update()
    {
        // Aquí va la lógica que se repite constantemente
        transform.Translate(Vector3.forward * Time.deltaTime);
    }
}
```

### Explicación línea por línea

```csharp
using UnityEngine;
```

* Permite usar todas las clases y funciones de Unity (Transform, GameObject, Debug, Input, etc.).

```csharp
public class MiPrimerScript : MonoBehaviour
```

* Define tu clase de script.
* `MonoBehaviour` es la **clase base** que permite que el script funcione como componente de Unity.

```csharp
void Start()
```

* Método que **se ejecuta una sola vez al inicio** (cuando el objeto se activa).

```csharp
void Update()
```

* Método que se llama **cada frame**. Ideal para movimientos, input y lógica continua.

```csharp
Debug.Log("Hola Mundo");
```

* Imprime un mensaje en la **Consola** de Unity. Muy útil para depurar.

```csharp
transform.Translate(Vector3.forward * Time.deltaTime);
```

* Mueve el objeto **hacia adelante** suavemente (dependiente del tiempo de frame).

* * *

### 🧠 **Métodos más comunes de MonoBehaviour**

| Método | Cuándo se llama | Para qué sirve |
| --- | --- | --- |
| `Awake()` | Al cargar el objeto, antes de Start | Inicialización de variables y referencias. |
| `Start()` | Antes del primer frame | Inicialización de lógica de juego. |
| `Update()` | Cada frame | Lógica de movimiento, input, animaciones continuas. |
| `FixedUpdate()` | Cada frame fijo de física | Movimiento con Rigidbody y cálculos de física. |
| `LateUpdate()` | Después de Update | Para cámaras o lógica que depende de otros objetos. |
| `OnEnable()` | Al activar el objeto | Inicializaciones temporales. |
| `OnDisable()` | Al desactivar el objeto | Limpiar referencias o detener acciones. |

* * *

### 🔹 **Variables públicas y privadas**

```csharp
public float velocidad = 5f;   // Visible en Inspector
private int vida = 100;        // Solo accesible dentro del script
[SerializeField] private string nombre = "LechuDev"; // Privada pero visible en Inspector
```

* `public` → editable desde el **Inspector**.
* `private` → solo dentro del script.
* `[SerializeField] private` → mantiene privacidad pero se puede ajustar en Inspector.

* * *

### 🔧 **Asociar Scripts a GameObjects**

1. Arrastra el script desde el **Project** al objeto en la **Hierarchy**.
2. Aparece como un **componente** en el **Inspector**.
3. Ahora puedes modificar las variables públicas directamente desde el Inspector.

💡 Esto permite crear instancias de objetos con comportamientos diferentes sin duplicar código.

* * *

### 🔹 **Instanciar objetos con Scripts**

```csharp
using UnityEngine;

public class Spawner : MonoBehaviour
{
    public GameObject prefabEnemigo;

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            Instantiate(prefabEnemigo, transform.position, Quaternion.identity);
        }
    }
}
```

* Presionar **Espacio** crea una copia del prefab en la escena.
* Los scripts dentro del prefab también se ejecutan automáticamente en la instancia.

* * *

### 🔹 **Buenas prácticas con Scripts**

1. **Separa lógica en scripts pequeños** → un script para movimiento, otro para salud, otro para animación.
2. **Usa variables públicas solo cuando necesites modificarlas desde Inspector**.
3. **Evita usar `Find()` constantemente** → consume recursos; usa referencias directas si es posible.
4. **Usa `SerializeField`** para mantener limpieza en el Inspector.
5. **Comenta tu código** → en proyectos grandes, esto salva vidas 😅.

* * *

### 🎯 Resumen

* Un **Script** da vida a los GameObjects.
* Se asocia como componente a un objeto.
* Usa `MonoBehaviour` para métodos clave (`Start`, `Update`, `FixedUpdate`).
* Las variables públicas aparecen en el Inspector y las privadas no (a menos que uses `[SerializeField]`).
* Permiten instanciación dinámica, lógica de juego y comunicación entre objetos.

* * *

## 🧩 **MonoBehaviour y sus métodos clave**

`MonoBehaviour` es la **clase base de todos los scripts que quieres que funcionen como componentes en Unity**.  
Si un script no hereda de `MonoBehaviour`, no puede usar métodos como `Start()`, `Update()` ni ser agregado como componente.

Dentro de `MonoBehaviour` hay **muchos métodos “callback”** que Unity llama automáticamente en diferentes momentos del ciclo de vida de un objeto. Vamos a verlos con detalle:

* * *

### 🔹 **1\. Awake()**

```csharp
void Awake()
{
    Debug.Log("Awake llamado");
}
```

* Se llama **cuando el objeto se carga**, antes de que el juego comience y antes de `Start()`.
* Ideal para **inicializar referencias** que otros scripts podrían necesitar.
* Se ejecuta incluso si el objeto está desactivado (activo en escena pero deshabilitado).

* * *

### 🔹 **2\. OnEnable()**

```csharp
void OnEnable()
{
    Debug.Log("Objeto activado");
}
```

* Se llama **cada vez que el objeto se activa** en la escena.
* Perfecto para **suscribirse a eventos** o activar lógica temporal.

* * *

### 🔹 **3\. Start()**

```csharp
void Start()
{
    Debug.Log("Start llamado");
}
```

* Se ejecuta **una vez, al inicio del primer frame en que el objeto está activo**.
* Ideal para inicializaciones **dependientes de otros objetos o scripts**, ya que `Awake` puede ejecutarse antes de que otros objetos existan.

* * *

### 🔹 **4\. Update()**

```csharp
void Update()
{
    Debug.Log("Update llamado cada frame");
}
```

* Se llama **cada frame del juego**.
* Ideal para:
  * Lectura de input (teclado, ratón, touch)
  * Movimientos continuos
  * Lógica que debe ocurrir constantemente

> ⚠️ Importante: si tu juego depende de **física**, mejor usar `FixedUpdate()` para movimientos de Rigidbody.

* * *

### 🔹 **5\. FixedUpdate()**

```csharp
void FixedUpdate()
{
    Debug.Log("FixedUpdate: sincronizado con física");
}
```

* Se ejecuta **cada frame fijo de física** (por defecto 0.02 segundos = 50 Hz).
* Ideal para:
  * Aplicar fuerzas a Rigidbody (`AddForce`)
  * Movimiento basado en física
  * Evitar problemas de inconsistencias al variar el FPS

* * *

### 🔹 **6\. LateUpdate()**

```csharp
void LateUpdate()
{
    Debug.Log("LateUpdate llamado después de Update");
}
```

* Se llama **después de todos los `Update()` de la escena**.
* Ideal para **cámaras que siguen objetos**, animaciones que dependen de movimientos calculados en `Update`.

* * *

### 🔹 **7\. OnDisable()**

```csharp
void OnDisable()
{
    Debug.Log("Objeto desactivado");
}
```

* Se llama cuando un objeto se desactiva.
* Útil para **desuscribirse de eventos**, detener corutinas o limpiar referencias.

* * *

### 🔹 **8\. OnDestroy()**

```csharp
void OnDestroy()
{
    Debug.Log("Objeto destruido");
}
```

* Se llama justo antes de que un objeto sea destruido con `Destroy()`.
* Perfecto para **limpieza final** (desasignar referencias, destruir hijos, detener corutinas).

* * *

### 🔹 **9\. Métodos de colisión y trigger**

```csharp
void OnCollisionEnter(Collision collision)
{
    Debug.Log("Colisión con: " + collision.gameObject.name);
}

void OnTriggerEnter(Collider other)
{
    Debug.Log("Trigger con: " + other.gameObject.name);
}
```

* Permiten detectar **colisiones físicas o triggers**.
* Fundamental para enemigos, pickups, balas, etc.

* * *

### 🔹 **Resumen de flujo de ejecución**

1. **Awake** → inicialización básica (antes de todo)
2. **OnEnable** → cuando se activa
3. **Start** → inicialización dependiente de otros objetos
4. **Update** → lógica por frame
5. **FixedUpdate** → lógica de física
6. **LateUpdate** → lógica post-Update, cámaras
7. **OnDisable** → limpieza al desactivar
8. **OnDestroy** → limpieza final al destruir

> 🔹 Tip: los callbacks de MonoBehaviour son **automáticos**, no los llamas tú directamente.

* * *

## 🧩 **Variables públicas y privadas**

Las variables en Unity determinan qué puedes editar desde el **Inspector** y qué queda oculto para mantener encapsulación.

### 🔹 **Public**

```csharp
public float velocidad = 5f;
```

* Aparece en el Inspector.
* Editable directamente en Unity.
* Accesible desde otros scripts.

### 🔹 **Private**

```csharp
private int vida = 100;
```

* No aparece en el Inspector.
* Solo accesible dentro del script.

### 🔹 **\[SerializeField\] Private**

```csharp
[SerializeField] private string nombre = "LechuDev";
```

* Mantiene la variable privada (otros scripts no pueden acceder).
* Pero **aparece en el Inspector**, útil para edición sin romper encapsulación.

* * *

### 🔹 **Otros modificadores útiles**

| Modificador | Efecto |
| --- | --- |
| `static` | La variable pertenece a la clase, no a instancias. |
| `const` | Valor constante que no cambia en tiempo de ejecución. |
| `readonly` | Similar a const, pero asignable en constructor o Awake. |

* * *

### 💡 Ejemplo práctico

```csharp
using UnityEngine;

public class Jugador : MonoBehaviour
{
    public float velocidad = 5f;      // editable desde Inspector
    [SerializeField] private int vida = 100; // privado pero editable
    private bool estaVivo = true;     // solo interno

    void Start()
    {
        Debug.Log("Jugador listo con vida: " + vida);
    }

    void Update()
    {
        float move = Input.GetAxis("Horizontal") * velocidad * Time.deltaTime;
        transform.Translate(move, 0, 0);
    }

    void OnCollisionEnter(Collision col)
    {
        if (col.gameObject.tag == "Enemigo")
        {
            vida -= 10;
            Debug.Log("Golpe recibido, vida: " + vida);
        }
    }
}
```

* `velocidad` → puedes ajustarla desde Inspector para probar sin tocar código.
* `vida` → editable, pero sigue siendo privado para otros scripts.
* `estaVivo` → interno, no visible, controla lógica interna.

* * *

## 🧩 **UI en Unity**

La **UI (User Interface)** en Unity es todo lo que permite que el jugador **interactúe o reciba información visual** dentro del juego.

* Se construye usando **GameObjects especiales** dentro de un **Canvas**.
* Permite crear **elementos 2D que se superponen a la escena 3D**, como HUDs o menús.
* Es completamente **configurable, escalable y animable**.

* * *

### 🔹 **Componentes principales de la UI**

#### 1\. **Canvas**

* Es la **base de toda UI**. Todo elemento UI debe estar dentro de un canvas.
* Controla cómo se renderizan los elementos en pantalla.

**Tipos de Render Mode en Canvas:**

| Tipo | Descripción |
| --- | --- |
| **Screen Space - Overlay** | UI siempre visible sobre la cámara, independiente del mundo. Ideal para HUDs y menús. |
| **Screen Space - Camera** | UI renderizada frente a una cámara específica. Permite efectos de profundidad. |
| **World Space** | UI en 3D, como paneles dentro de la escena que se comportan como objetos normales. |

* * *

#### 2\. **Panel**

* Objeto contenedor de UI (`Right Click → UI → Panel`).
* Sirve para agrupar elementos.
* Se puede usar para menús, fondos de ventanas o secciones de HUD.
* Puede tener **imagen de fondo, color, transparencia, efectos**.

* * *

#### 3\. **Text / TextMeshPro**

* Muestra **texto en pantalla**.
* `TextMeshPro` es la versión avanzada y recomendada: mejor calidad, escalabilidad y opciones tipográficas.
* Se puede usar para puntuaciones, diálogos o nombres de personajes.

* * *

#### 4\. **Button (Botón)**

* Elemento interactivo que puede disparar **eventos** al hacer clic.
* Se configura con:
  * Texto (child Text)
  * Color en estados normal, hover, presionado
  * Función asociada (`OnClick()` → arrastrar GameObject con script → método público)

* * *

#### 5\. **Image**

* Sirve para mostrar **sprites o gráficos** dentro de la UI.
* Útil para barras, iconos, fondos, máscaras, etc.

* * *

#### 6\. **Slider**

* Barra deslizante, útil para:
  * Volumen, vida, progreso, energía, etc.
* Configurable: rango mínimo y máximo, valor inicial, evento `OnValueChanged`.

* * *

#### 7\. **Toggle (Casilla / Switch)**

* Elemento de **encendido/apagado**.
* Ej: activar/desactivar música, opciones, poder o habilidad.

* * *

#### 8\. **Input Field**

* Campo para ingresar texto por el usuario.
* Configurable: tipo de contenido, longitud máxima, placeholder, eventos `OnValueChanged` o `OnEndEdit`.

* * *

#### 9\. **Dropdown**

* Menú desplegable para seleccionar opciones.
* Configurable: lista de opciones, valor inicial, evento `OnValueChanged`.

* * *

#### 10\. **Scroll Rect**

* Permite crear **listas desplazables**.
* Muy útil para inventarios, menús extensos o mapas.

* * *

### 🔹 **Configuraciones y jerarquía en UI**

* Todos los elementos UI **deben estar hijos de un Canvas**.
* Jerarquía típica:

```yaml
Canvas
├── Panel_HUD
│   ├── Image_Vida
│   ├── Text_Puntos
│   └── Button_Pausa
├── Panel_Menu
│   ├── Button_Jugar
│   ├── Button_Opciones
│   └── Button_Salir
```

* Se puede usar **Empty GameObject dentro del Canvas** como contenedor para organizar elementos.
* **Anchors y Pivot Points**: controlan la posición relativa y escalado de elementos UI en diferentes resoluciones.

* * *

### 🔹 **Eventos en UI**

* Unity usa un sistema llamado **EventSystem**, que gestiona **clics, toques y movimientos de cursor** sobre la UI.
* Todos los botones, sliders y toggles dependen de esto para **disparar eventos**.

**Ejemplo de botón con script:**

```csharp
using UnityEngine;
using UnityEngine.UI;

public class Menu : MonoBehaviour
{
    public Button miBoton;

    void Start()
    {
        miBoton.onClick.AddListener(PresionarBoton);
    }

    void PresionarBoton()
    {
        Debug.Log("Botón presionado");
    }
}
```

* `onClick.AddListener()` → conecta el botón a un método público.
* Permite **interacción dinámica desde código**.

* * *

### 🔹 **Tips profesionales para UI**

1. Usa **TextMeshPro** en vez del texto básico por claridad y escalabilidad.
2. Mantén la UI **organizada en paneles y contenedores**.
3. Usa **Anchors y Pivots** para que la UI se adapte a cualquier resolución.
4. Prefabs para UI → los menús, botones o HUDs recurrentes pueden guardarse como Prefabs.
5. EventSystem siempre debe existir en la escena para que la UI funcione. Unity lo agrega automáticamente al crear un Canvas.

* * *

### 🔹 **Resumen rápido**

* **Canvas:** base de toda UI, define cómo se renderiza.
* **Panel:** contenedor de elementos UI.
* **Elementos comunes:** Text/TextMeshPro, Image, Button, Slider, Toggle, InputField, Dropdown, Scroll Rect.
* **Eventos:** gestionados por EventSystem y scripts (`onClick`, `OnValueChanged`).
* **Organización:** jerarquía + anchors + pivots para adaptabilidad.

* * *

## 🧩 **Cambiar entre escenas**

🧩 **Requisitos previos**

1. Tener **varias escenas creadas** en tu proyecto.
    * Por ejemplo: `MenuPrincipal`, `Nivel1`, `Nivel2`.
2. Asegurarte de que las escenas estén **agregadas en Build Settings**:
    * Ve a `File → Build Settings`
    * Presiona **Add Open Scenes** para cada escena que quieras cargar.

> ⚠️ Cada escena necesita un **índice** o nombre para poder ser cargada desde código.

* * *

### 🔹 **Paso 1: Crear el botón en la UI**

1. En tu **Canvas**, clic derecho → `UI → Button`.
2. Se crea un botón con un objeto hijo **Text** (puedes renombrarlo a `BtnJugar` por ejemplo).
3. Ajusta posición, tamaño y texto desde el **Inspector**.

* * *

### 🔹 **Paso 2: Crear un Script para manejar la escena**

Crea un script llamado, por ejemplo, `ControlEscenas.cs`:

```csharp
using UnityEngine;
using UnityEngine.SceneManagement; // Necesario para cargar escenas

public class ControlEscenas : MonoBehaviour
{
    // Método público para cambiar de escena por nombre
    public void CambiarEscena(string nombreEscena)
    {
        SceneManager.LoadScene(nombreEscena);
    }

    // Método público para cambiar de escena por índice
    public void CambiarEscena(int indiceEscena)
    {
        SceneManager.LoadScene(indiceEscena);
    }
}
```

#### Explicación

* `using UnityEngine.SceneManagement;` → importa el namespace que contiene funciones para **manejar escenas**.
* `SceneManager.LoadScene(...)` → carga la escena indicada (por nombre o índice).
* Los métodos son **públicos** para que puedan conectarse desde el **Inspector** a un botón.

* * *

### 🔹 **Paso 3: Asignar el script al botón**

1. Crea un **Empty GameObject** en la escena, renómbralo por ejemplo a `GestorEscenas`.
2. Arrastra el script `ControlEscenas` al **Inspector** de ese objeto.
3. Selecciona el botón (`BtnJugar`) → en el **Inspector**, busca la sección `Button (Script)` → `OnClick()`.
4. Presiona `+` para agregar un evento.
5. Arrastra el objeto `GestorEscenas` al campo vacío que aparece.
6. En el desplegable, selecciona `ControlEscenas → CambiarEscena(string)`.
7. Escribe el **nombre exacto de la escena** que quieres cargar (por ejemplo: `Nivel1`).

> ✅ Ahora al presionar el botón, Unity cargará la escena indicada.

* * *

### 🔹 **Paso 4: Opciones avanzadas**

* **Cambiar por índice:**
  * Cada escena tiene un **Build Index** en Build Settings.
  * Puedes llamar `CambiarEscena(1)` para cargar la escena con índice 1.
* **Transiciones con animaciones:**
  * Puedes agregar un `Animator` al Canvas o usar un **Panel negro** que se desvanezca para un efecto de fade.
* **Cargar escenas asincrónicamente (para niveles grandes):**

```csharp
public void CambiarEscenaAsync(string nombreEscena)
{
    StartCoroutine(CargarEscena(nombreEscena));
}

IEnumerator CargarEscena(string nombreEscena)
{
    AsyncOperation asyncLoad = SceneManager.LoadSceneAsync(nombreEscena);

    while (!asyncLoad.isDone)
    {
        // Aquí puedes actualizar un loading bar si quieres
        yield return null;
    }
}
```

* * *

### 🔹 **Tips importantes**

1. **Asegúrate de que el nombre de la escena coincide exactamente** con el de Build Settings.
2. **No olvides agregar la escena a Build Settings**, de lo contrario no cargará.
3. **Usa métodos públicos** en scripts para conectarlos a botones sin tener que usar `Find` o referencias complicadas.
4. **Para UI dinámica**, puedes tener un `ControlEscenas` central que maneje todos los botones y transiciones.

* * *

## 🧩 **Capsule Collider en Unity**

Un **Capsule Collider** es un componente de física que **define un volumen en forma de cápsula** alrededor de un objeto.

* Este volumen **detecta colisiones** con otros colliders.
* Es común en personajes humanos o humanoides porque su forma se asemeja a un cuerpo vertical.
* No se ve en el juego; solo aparece como un **gizmo en la Scene**.

* * *

### **Para qué sirve

1. **Detección de colisiones** con el entorno (suelo, paredes, obstáculos).
2. **Interacción con físicas**: si el objeto tiene Rigidbody, el collider permite empujar, caer o ser afectado por fuerzas.
3. **Triggers**: puede actuar como área de detección sin física, usando `isTrigger`.

Ejemplos típicos:

* Personaje jugador → Capsule Collider vertical para caminar y saltar.
* NPC → mismo collider para detectar obstáculos.
* Zona de daño → usar como trigger para activar efectos al entrar.

* * *

### Configuración del Capsule Collider

Cuando agregas un Capsule Collider (`Add Component → Physics → Capsule Collider`), verás estas propiedades:

| Propiedad | Función |
| --- | --- |
| **Center** | Posición del centro del collider relativo al objeto. Permite ajustar que el collider quede alineado con el cuerpo. |
| **Radius** | Radio de la cápsula. Controla el ancho. |
| **Height** | Altura de la cápsula. Junto con el radio, define el volumen total. |
| **Direction** | Eje de la cápsula (X, Y o Z). Normalmente Y para personajes verticales. |
| **Is Trigger** | Si está activado, el collider no genera colisiones físicas, solo eventos `OnTriggerEnter/Exit`. |
| **Material** | Asigna un **Physics Material** para controlar fricción y rebote. |

* * *

### Ejemplo visual de propiedades

* **Direction: Y** → cápsula vertical (personaje).
* **Radius: 0.5** → ancho del cuerpo.
* **Height: 2** → altura del personaje.
* **Center: (0,1,0)** → coloca el collider centrado sobre el modelo.

> Si el personaje está inclinado o acostado, cambiar **Direction** a X o Z puede ser útil.

* * *

### Uso con Rigidbody

Para que el Capsule Collider interactúe con físicas:

1. Agrega un **Rigidbody** al mismo objeto.
2. Configura propiedades:
    * **Mass:** masa del objeto.
    * **Drag / Angular Drag:** resistencia lineal y angular.
    * **Use Gravity:** si debe caer.
    * **Is Kinematic:** si controlas movimiento manualmente (desactiva físicas automáticas).
        * Ejemplo típico: personaje jugador con Capsule Collider + Rigidbody + script de movimiento.

* * *

### Eventos importantes con Capsule Collider

* **Colisiones normales:**

```csharp
void OnCollisionEnter(Collision col)
{
    Debug.Log("Chocó con: " + col.gameObject.name);
}
```

* **Triggers:**

```csharp
void OnTriggerEnter(Collider other)
{
    Debug.Log("Entró en trigger: " + other.gameObject.name);
}
```

> ⚠️ Para triggers, asegúrate de marcar **Is Trigger = true**.

* * *

### Tips profesionales

1. **Siempre ajusta Center, Radius y Height** según el modelo 3D, no uses valores por defecto.
2. **No uses colisiones demasiado grandes o pequeñas**, pueden causar que el personaje quede atrapado en paredes o atraviese objetos.
3. Para personajes humanos, **Direction Y** es estándar.
4. Para detectar el suelo, puedes usar un collider hijo más pequeño o un raycast desde el pie.
5. **Physics Materials** ayudan a que el personaje no “resbale” o rebote exageradamente.

* * *

### 💡 **Resumen rápido**

* **Capsule Collider:** volumen de colisión en forma de cápsula.
* **Usos:** personajes, NPCs, triggers, interacciones físicas.
* **Propiedades clave:** Center, Radius, Height, Direction, Is Trigger, Material.
* **Combinación típica:** Capsule Collider + Rigidbody + Script de movimiento.

* * *

## 🧩 **Rigidbody en Unity**

Un **Rigidbody** es un **componente de física** que convierte un GameObject en un **objeto afectado por la simulación física de Unity**.

* Sin Rigidbody, los colliders solo detectan colisiones pero no reaccionan físicamente.
* Con Rigidbody, el objeto puede moverse, caer, rebotar y recibir fuerzas como empujones.
* Es fundamental para personajes, proyectiles, objetos interactivos y cualquier cosa que deba comportarse de forma realista.

* * *

### **Agregar un Rigidbody**

1. Selecciona un GameObject.
2. `Add Component → Physics → Rigidbody`.
3. Se habilitan sus propiedades en el **Inspector**.

* * *

### **Propiedades principales**

| Propiedad | Función |
| --- | --- |
| **Mass** | Masa del objeto (influyen fuerzas y gravedad). |
| **Drag** | Resistencia lineal, frena movimiento como “rozamiento del aire”. |
| **Angular Drag** | Resistencia a rotación. |
| **Use Gravity** | Si está activado, el objeto cae según la gravedad del mundo. |
| **Is Kinematic** | Si está activo, el Rigidbody **ignora física**, solo se mueve con código o animaciones. |
| **Interpolate** | Suaviza movimiento visual entre frames, útil para objetos rápidos. |
| **Collision Detection** | Cómo detectar colisiones para objetos rápidos: `Discrete`, `Continuous`, `Continuous Dynamic`. |

* * *

### **Tipos de movimiento con Rigidbody**

#### 1\. **Movimiento físico**

```csharp
Rigidbody rb = GetComponent<Rigidbody>();
rb.AddForce(Vector3.forward * 500f);
```

* Aplica una **fuerza continua**.
* Afecta a la física y la colisión automáticamente.

#### 2\. **Movimiento directo (transform)**

```csharp
transform.Translate(Vector3.forward * Time.deltaTime * 5f);
```

* Mueve el objeto **sin usar física real**.
* No debe usarse si el Rigidbody está activo y quieres colisiones naturales.

> ⚠️ Para objetos con Rigidbody activo, **moverlos por transform** puede causar que atraviesen colisiones.

* * *

### **Métodos útiles del Rigidbody**

| Método | Función |
| --- | --- |
| `AddForce(Vector3 fuerza)` | Aplica fuerza sobre el objeto (Newton). |
| `AddTorque(Vector3 torque)` | Aplica rotación o torsión. |
| `MovePosition(Vector3 posición)` | Mueve Rigidbody a una posición, respetando física. |
| `MoveRotation(Quaternion rotación)` | Rota Rigidbody respetando física. |
| `Sleep()` / `WakeUp()` | Pone el objeto en reposo o lo reactiva. |

* * *

### **Propiedades avanzadas**

* **Interpolate**
  * `None` → movimiento sin suavizado.
  * `Interpolate` → suaviza entre frames, reduce jitter.
  * `Extrapolate` → predice la posición futura, útil para objetos muy rápidos.
* **Collision Detection**
  * `Discrete` → colisiones simples por frame (default).
  * `Continuous` → evita que objetos rápidos atraviesen otros.
  * `Continuous Dynamic` → para proyectiles o jugadores rápidos.
* **Constraints**
  * Puedes **bloquear rotación o posición** en X, Y, Z para controlar movimiento.
  * Ejemplo: personaje humano → bloquear rotación X y Z para que no se caiga.

* * *

### **Ejemplo práctico de Rigidbody**

```csharp
using UnityEngine;

public class BolaFisica : MonoBehaviour
{
    public Rigidbody rb;
    public float fuerza = 500f;

    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            // Aplica una fuerza hacia adelante
            rb.AddForce(Vector3.forward * fuerza);
        }
    }
}
```

### Explicación del Ejemplo de Rigidbody

* `rb = GetComponent<Rigidbody>();` → referencia al Rigidbody del objeto.
* `AddForce` → empuja la bola usando física.
* Input `Space` → cada vez que presionas, la fuerza se aplica.

💡 Esto simula un **proyectil, pelota o empuje de personaje** sin mover directamente el transform.

* * *

### **Rigidbody + Colliders**

* El Rigidbody **funciona mejor con un collider**.
* Ejemplos comunes:
  * Personaje humano → Capsule Collider + Rigidbody.
  * Bola → Sphere Collider + Rigidbody.
  * Caja → Box Collider + Rigidbody.
* Si quieres solo detectar colisiones **sin afectar física**, activa **Is Kinematic** o usa **triggers**.

* * *

### **Tips profesionales**

1. Para personajes controlados por código, **bloquea rotaciones innecesarias** (`Constraints → Freeze Rotation X/Z`).
2. Usa `Interpolate` para **suavizar movimiento** visual.
3. Para proyectiles rápidos, usa `Collision Detection → Continuous Dynamic`.
4. Evita mover Rigidbody directamente con `transform` si quieres física natural.
5. Combina Rigidbody con **Animator o scripts** para crear personajes que reaccionan a fuerzas físicas y animaciones.

* * *

### 💡 **Resumen rápido de Rigidbody**

* **Rigidbody:** hace que un objeto sea afectado por física y gravedad.
* **Propiedades clave:** Mass, Drag, Angular Drag, Use Gravity, Is Kinematic.
* **Métodos:** AddForce, AddTorque, MovePosition, MoveRotation.
* **Consejo:** siempre combinar con un collider adecuado.
* **Uso típico:** personajes, proyectiles, NPCs, objetos interactivos.

* * *

## indice

1. [Curso de Unity básico](#curso-de-unity-básico)
   1. [Introducción](#introducción)
   2. [1. Qué es Unity](#1-qué-es-unity)
   3. [2. Qué es Unity Hub](#2-qué-es-unity-hub)
   4. [3. Instalación de Unity](#3-instalación-de-unity)
   5. [4. Diferencias entre versiones de Unity](#4-diferencias-entre-versiones-de-unity)
   6. [5. Plataformas para las que puede compilar Unity](#5-plataformas-para-las-que-puede-compilar-unity)
   7. [6. Build y estructuras básicas de proyectos en Unity](#6-build-y-estructuras-básicas-de-proyectos-en-unity)
      1. [1. Plantillas de proyecto (Project Templates)](#1-plantillas-de-proyecto-project-templates)
      2. [2. Estructura básica de un proyecto de Unity](#2-estructura-básica-de-un-proyecto-de-unity)
   8. [7. Cómo crear un proyecto 3D en Unity](#7-cómo-crear-un-proyecto-3d-en-unity)
      1. [**Paso 1: Abrir Unity Hub**](#paso-1-abrir-unity-hub)
      2. [**Paso 2: Seleccionar la opción para crear un nuevo proyecto**](#paso-2-seleccionar-la-opción-para-crear-un-nuevo-proyecto)
      3. [**Paso 3: Elegir la plantilla del proyecto**](#paso-3-elegir-la-plantilla-del-proyecto)
      4. [**Paso 4: Configurar el nombre y ubicación**](#paso-4-configurar-el-nombre-y-ubicación)
      5. [**Paso 5: Crear el proyecto**](#paso-5-crear-el-proyecto)
      6. [**Paso 6: Familiarizarse con la interfaz**](#paso-6-familiarizarse-con-la-interfaz)
   9. [8. Entradas en Unity](#8-entradas-en-unity)
      1. [8.1 🧠 ¿Qué es el Input Manager?](#81--qué-es-el-input-manager)
         1. [⚙️ ¿Cómo acceder al Input Manager?](#️-cómo-acceder-al-input-manager)
         2. [🛠️ Estructura del Input Manager](#️-estructura-del-input-manager)
         3. [🎮 ¿Para qué se utiliza?](#-para-qué-se-utiliza)
         4. [⚠️ Consideraciones](#️-consideraciones)
      2. [8.2 🧠 ¿Qué es el Input System?](#82--qué-es-el-input-system)
         1. [⚙️ ¿Cómo instalarlo?](#️-cómo-instalarlo)
         2. [🧩 Conceptos clave](#-conceptos-clave)
         3. [🎮 Flujo básico de uso](#-flujo-básico-de-uso)
         4. [🛠️ Características avanzadas](#️-características-avanzadas)
      3. [8.3 1️⃣ Uso básico del Input Manager (clásico) explicado línea por línea](#83-1️⃣-uso-básico-del-input-manager-clásico-explicado-línea-por-línea)
      4. [8.4 2️⃣ Uso básico del Input System (moderno) explicado línea por línea](#84-2️⃣-uso-básico-del-input-system-moderno-explicado-línea-por-línea)
      5. [8.5 💡 **Resumen comparativo rápido**](#85--resumen-comparativo-rápido)
   10. [9. Assets, GameObjects y Componentes](#9-assets-gameobjects-y-componentes)
       1. [**1️⃣ Qué son los Assets**](#1️⃣-qué-son-los-assets)
       2. [**2️⃣ Qué son los GameObjects**](#2️⃣-qué-son-los-gameobjects)
       3. [**3️⃣ Qué son los Componentes**](#3️⃣-qué-son-los-componentes)
   11. [10. **1️⃣ Qué es una cámara en Unity**](#10-1️⃣-qué-es-una-cámara-en-unity)
       1. [**2️⃣ Tipos de cámaras**](#2️⃣-tipos-de-cámaras)
       2. [**3️⃣ Para qué se usan**](#3️⃣-para-qué-se-usan)
       3. [**4️⃣ Cómo se crean y configuran**](#4️⃣-cómo-se-crean-y-configuran)
       4. [**Crear una cámara nueva**](#crear-una-cámara-nueva)
       5. [**Configurar sus propiedades principales**](#configurar-sus-propiedades-principales)
       6. [**Hacer que la cámara siga un objeto**](#hacer-que-la-cámara-siga-un-objeto)
   12. [11. \*\*2️⃣🎥 **¿Qué es Cinemachine?**](#11-2️⃣-qué-es-cinemachine)
       1. [🧩 **Cómo instalar Cinemachine**](#-cómo-instalar-cinemachine)
       2. [⚙️ **Cómo crear una cámara Cinemachine básica**](#️-cómo-crear-una-cámara-cinemachine-básica)
          1. [📍 Paso 1: Crear una cámara virtual](#-paso-1-crear-una-cámara-virtual)
          2. [📍 Paso 2: Asignar un objetivo (Follow y Look At)](#-paso-2-asignar-un-objetivo-follow-y-look-at)
          3. [📍 Paso 3: Ajustar el comportamiento de la cámara](#-paso-3-ajustar-el-comportamiento-de-la-cámara)
       3. [🎬 **Tipos de cámaras Cinemachine más usados**](#-tipos-de-cámaras-cinemachine-más-usados)
       4. [🧠 **Ejemplo básico con FreeLook Camera**](#-ejemplo-básico-con-freelook-camera)
       5. [💻 **Cinemachine en código (uso opcional)**](#-cinemachine-en-código-uso-opcional)
       6. [🎨 **Ventajas de usar Cinemachine**](#-ventajas-de-usar-cinemachine)
       7. [💡 **Consejos profesionales**](#-consejos-profesionales)
   13. [12. ☀️ **1️⃣ Qué son las luces en Unity**](#12-️-1️⃣-qué-son-las-luces-en-unity)
       1. [💡 **2️⃣ Tipos de luces en Unity**-](#-2️⃣-tipos-de-luces-en-unity-)
       2. [🛠️ **3️⃣ Cómo crear una luz**](#️-3️⃣-cómo-crear-una-luz)
       3. [📍 Método 1 – Desde el menú](#-método-1--desde-el-menú)
       4. [📍 Método 2 – Desde la jerarquía](#-método-2--desde-la-jerarquía)
       5. [⚙️ **4️⃣ Propiedades principales del componente Light**](#️-4️⃣-propiedades-principales-del-componente-light)
       6. [🌞 **5️⃣ Tipos de sombras**](#-5️⃣-tipos-de-sombras)
       7. [🔥 **6️⃣ Modos de iluminación: Real-Time, Mixed y Baked**](#-6️⃣-modos-de-iluminación-real-time-mixed-y-baked)
       8. [💻 **7️⃣ Ejemplo simple de luz dinámica con código**](#-7️⃣-ejemplo-simple-de-luz-dinámica-con-código)
       9. [🌗 **8️⃣ Luces y rendimiento**](#-8️⃣-luces-y-rendimiento)
       10. [✨ **9️⃣ Efectos y postprocesado**](#-9️⃣-efectos-y-postprocesado)
       11. [💡 **1️⃣0️⃣ Consejos finales**](#-1️⃣0️⃣-consejos-finales)
   14. [13. 🎬 **1️⃣ Qué es una Scene (Escena)**](#13--1️⃣-qué-es-una-scene-escena)
       1. [🧩 **2️⃣ Qué contiene una Scene**](#-2️⃣-qué-contiene-una-scene)
       2. [🏗️ **3️⃣ Dónde se guardan las Scenes**](#️-3️⃣-dónde-se-guardan-las-scenes)
       3. [⚙️ **4️⃣ Cómo crear una nueva Scene**](#️-4️⃣-cómo-crear-una-nueva-scene)
          1. [📍 Opción 1 – Desde el menú](#-opción-1--desde-el-menú)
          2. [📍 Opción 2 – Desde la jerarquía](#-opción-2--desde-la-jerarquía)
       4. [🧠 **5️⃣ Cómo abrir y cambiar de Scene**](#-5️⃣-cómo-abrir-y-cambiar-de-scene)
       5. [🔄 **6️⃣ Tipos de carga de escenas**](#-6️⃣-tipos-de-carga-de-escenas)
       6. [🧱 **7️⃣ Escena activa y administración**](#-7️⃣-escena-activa-y-administración)
       7. [🌍 **8️⃣ Scene View vs Game View**](#-8️⃣-scene-view-vs-game-view)
       8. [🔦 **9️⃣ Ejemplo: crear una escena completa desde cero**](#-9️⃣-ejemplo-crear-una-escena-completa-desde-cero)
       9. [💾 **🔟 Cómo agregar escenas al Build Settings**](#--cómo-agregar-escenas-al-build-settings)
       10. [⚡ **1️⃣1️⃣ Buenas prácticas**](#-1️⃣1️⃣-buenas-prácticas)
       11. [🧙‍♂️ **1️⃣2️⃣ Ejemplo de sistema de transición entre escenas con animación**](#️-1️⃣2️⃣-ejemplo-de-sistema-de-transición-entre-escenas-con-animación)
       12. [🎮 **1️⃣3️⃣Controles para moverte en la Escena (Scene View)**](#-1️⃣3️⃣controles-para-moverte-en-la-escena-scene-view)
           1. [🧭 Movimiento básico del punto de vista](#-movimiento-básico-del-punto-de-vista)
           2. [🧠 Consejillo pro](#-consejillo-pro)
   15. [14. ☀️ ¿Qué es el “Auto-Generating Lighting” en Unity?](#14-️-qué-es-el-auto-generating-lighting-en-unity)
       1. [⚙️ ¿Dónde está la opción?](#️-dónde-está-la-opción)
       2. [💡 Tipos de iluminación que intervienen](#-tipos-de-iluminación-que-intervienen)
       3. [🧱 ¿Qué se genera al “Bakear” la luz?](#-qué-se-genera-al-bakear-la-luz)
       4. [⚡ Cuándo usar Auto Generate o hacerlo manual](#-cuándo-usar-auto-generate-o-hacerlo-manual)
       5. [🌈 Consejos pro](#-consejos-pro)
   16. [15. 🧱 ¿Qué es un Material en Unity?](#15--qué-es-un-material-en-unity)
       1. [🌈 ¿De qué está hecho un Material?](#-de-qué-está-hecho-un-material)
       2. [Estructura básica de un Material](#estructura-básica-de-un-material)
       3. [🧩 ¿Dónde se crean y cómo se aplican?](#-dónde-se-crean-y-cómo-se-aplican)
       4. [🪄 Crear un nuevo Material](#-crear-un-nuevo-material)
       5. [🎨 Aplicar un Material a un objeto](#-aplicar-un-material-a-un-objeto)
       6. [⚙️ Tipos de Shaders más comunes](#️-tipos-de-shaders-más-comunes)
       7. [✨ Texturas (las "pinturas" del material)](#-texturas-las-pinturas-del-material)
       8. [🧠 Tips de uso](#-tips-de-uso)
   17. [16. 🧭 ¿Qué es el Componente Transform?](#16--qué-es-el-componente-transform)
       1. [📦 Estructura del Transform en el Inspector](#-estructura-del-transform-en-el-inspector)
       2. [🌎 Coordenadas locales vs globales](#-coordenadas-locales-vs-globales)
       3. [🧠 ¿Cómo manipular el Transform en código?](#-cómo-manipular-el-transform-en-código)
       4. [🧩 Ejemplo básico](#-ejemplo-básico)
       5. [🔍 Explicación línea por línea](#-explicación-línea-por-línea)
       6. [⚙️ Métodos útiles del Transform](#️-métodos-útiles-del-transform)
       7. [🎮 Ejemplo práctico: seguir un objetivo](#-ejemplo-práctico-seguir-un-objetivo)
       8. [🧱 Jerarquías y Transform hijo/padre](#-jerarquías-y-transform-hijopadre)
       9. [Ejemplo visual](#ejemplo-visual)
       10. [🧩 Manipulación avanzada (por código)](#-manipulación-avanzada-por-código)
       11. [💡 Tips finales](#-tips-finales)
   18. [17. 🧭 ¿Qué es el Inspector en Unity?](#17--qué-es-el-inspector-en-unity)
       1. [🧱 Estructura general del Inspector](#-estructura-general-del-inspector)
       2. [🎚️ Cómo usarlo eficientemente](#️-cómo-usarlo-eficientemente)
       3. [🔍 1. Editar propiedades en tiempo real](#-1-editar-propiedades-en-tiempo-real)
       4. [🧩 2. Arrastrar y soltar referencias](#-2-arrastrar-y-soltar-referencias)
       5. [🔒 3. Bloquear el Inspector](#-3-bloquear-el-inspector)
       6. [⚙️ 4. Menú de componentes](#️-4-menú-de-componentes)
       7. [🎨 Inspector en modo Play](#-inspector-en-modo-play)
       8. [🧠 Inspector y Scripts personalizados](#-inspector-y-scripts-personalizados)
       9. [🧰 Custom Inspectors (para pros)](#-custom-inspectors-para-pros)
       10. [⚡ Atajos útiles y trucos](#-atajos-útiles-y-trucos)
       11. [🧩 Ejemplo de flujo completo](#-ejemplo-de-flujo-completo)
       12. [🎯 En resumen](#-en-resumen)
   19. [18. 🧩 **La Consola de Unity**](#18--la-consola-de-unity)
       1. [📜 ¿Qué es la Consola?](#-qué-es-la-consola)
       2. [⚙️ ¿Dónde se encuentra?](#️-dónde-se-encuentra)
       3. [💬 Tipos de Mensajes en la Consola](#-tipos-de-mensajes-en-la-consola)
       4. [🔢 Tipos de Errores más comunes](#-tipos-de-errores-más-comunes)
          1. [🟥 1. **Errores de Compilación**](#-1-errores-de-compilación)
          2. [🟨 2. **Warnings (Advertencias)**](#-2-warnings-advertencias)
          3. [⚪ 3. **Logs e Información**](#-3-logs-e-información)
       5. [🧰 Botones y Filtros de la Consola](#-botones-y-filtros-de-la-consola)
       6. [🧠 Consejos Pro para Usarla Bien](#-consejos-pro-para-usarla-bien)
       7. [🧩 Bonus: Depuración en Tiempo Real](#-bonus-depuración-en-tiempo-real)
       8. [🧭 En Resumen](#-en-resumen-1)
   20. [19. 🧱 **La Ventana Hierarchy (Jerarquía)**](#19--la-ventana-hierarchy-jerarquía)
       1. [🧩 ¿Qué es?](#-qué-es)
       2. [🧠 Ejemplo visual](#-ejemplo-visual)
       3. [⚙️ Acciones básicas](#️-acciones-básicas)
       4. [🧭 Tips profesionales](#-tips-profesionales)
   21. [20. 📦 **La Ventana Project (Proyecto)**](#20--la-ventana-project-proyecto)
       1. [📁 ¿Qué es?](#-qué-es-1)
       2. [🗂️ Estructura típica de carpetas](#️-estructura-típica-de-carpetas)
       3. [⚙️ Acciones útiles en el Project](#️-acciones-útiles-en-el-project)
       4. [🧠 Relación entre Project y Hierarchy](#-relación-entre-project-y-hierarchy)
       5. [🎓 Pro Tip](#-pro-tip)
       6. [🔎 Diferencias rápidas](#-diferencias-rápidas)
       7. [🧩 En Resumen](#-en-resumen-2)
   22. [🧩 **Ventanas principales de Unity**](#-ventanas-principales-de-unity)
       1. [1️⃣ **Scene Window (Escena)**](#1️⃣-scene-window-escena)
       2. [2️⃣ **Game Window (Juego)**](#2️⃣-game-window-juego)
       3. [3️⃣ **Other Useful Windows (Otras ventanas útiles)**](#3️⃣-other-useful-windows-otras-ventanas-útiles)
       4. [🔹 Organización de ventanas](#-organización-de-ventanas)
       5. [💡 Tipos de uso](#-tipos-de-uso)
   23. [🧩 **¿Qué es un Prefab?**](#-qué-es-un-prefab)
       1. [🧱 **Ventajas de usar Prefabs**](#-ventajas-de-usar-prefabs)
       2. [⚙️ **Cómo crear un Prefab**](#️-cómo-crear-un-prefab)
       3. [🧠 **Tipos de Prefab en Unity 2025**](#-tipos-de-prefab-en-unity-2025)
       4. [🔹 **Instanciar Prefabs por código**](#-instanciar-prefabs-por-código)
       5. [🧩 **Editar Prefabs**](#-editar-prefabs)
       6. [⚡ **Tips Profesionales**](#-tips-profesionales-1)
   24. [🧩 **¿Qué es un Script en Unity?**](#-qué-es-un-script-en-unity)
       1. [🧱 **Estructura básica de un Script en Unity (C#)**](#-estructura-básica-de-un-script-en-unity-c)
       2. [Explicación línea por línea](#explicación-línea-por-línea)
       3. [🧠 **Métodos más comunes de MonoBehaviour**](#-métodos-más-comunes-de-monobehaviour)
       4. [🔹 **Variables públicas y privadas**](#-variables-públicas-y-privadas)
       5. [🔧 **Asociar Scripts a GameObjects**](#-asociar-scripts-a-gameobjects)
       6. [🔹 **Instanciar objetos con Scripts**](#-instanciar-objetos-con-scripts)
       7. [🔹 **Buenas prácticas con Scripts**](#-buenas-prácticas-con-scripts)
       8. [🎯 Resumen](#-resumen)
   25. [🧩 **MonoBehaviour y sus métodos clave**](#-monobehaviour-y-sus-métodos-clave)
       1. [🔹 **1. Awake()**](#-1-awake)
       2. [🔹 **2. OnEnable()**](#-2-onenable)
       3. [🔹 **3. Start()**](#-3-start)
       4. [🔹 **4. Update()**](#-4-update)
       5. [🔹 **5. FixedUpdate()**](#-5-fixedupdate)
       6. [🔹 **6. LateUpdate()**](#-6-lateupdate)
       7. [🔹 **7. OnDisable()**](#-7-ondisable)
       8. [🔹 **8. OnDestroy()**](#-8-ondestroy)
       9. [🔹 **9. Métodos de colisión y trigger**](#-9-métodos-de-colisión-y-trigger)
       10. [🔹 **Resumen de flujo de ejecución**](#-resumen-de-flujo-de-ejecución)
   26. [🧩 **Variables públicas y privadas**](#-variables-públicas-y-privadas-1)
       1. [🔹 **Public**](#-public)
       2. [🔹 **Private**](#-private)
       3. [🔹 **\[SerializeField\] Private**](#-serializefield-private)
       4. [🔹 **Otros modificadores útiles**](#-otros-modificadores-útiles)
       5. [💡 Ejemplo práctico](#-ejemplo-práctico)
   27. [🧩 **UI en Unity**](#-ui-en-unity)
       1. [🔹 **Componentes principales de la UI**](#-componentes-principales-de-la-ui)
          1. [1. **Canvas**](#1-canvas)
          2. [2. **Panel**](#2-panel)
          3. [3. **Text / TextMeshPro**](#3-text--textmeshpro)
          4. [4. **Button (Botón)**](#4-button-botón)
          5. [5. **Image**](#5-image)
          6. [6. **Slider**](#6-slider)
          7. [7. **Toggle (Casilla / Switch)**](#7-toggle-casilla--switch)
          8. [8. **Input Field**](#8-input-field)
          9. [9. **Dropdown**](#9-dropdown)
          10. [10. **Scroll Rect**](#10-scroll-rect)
       2. [🔹 **Configuraciones y jerarquía en UI**](#-configuraciones-y-jerarquía-en-ui)
       3. [🔹 **Eventos en UI**](#-eventos-en-ui)
       4. [🔹 **Tips profesionales para UI**](#-tips-profesionales-para-ui)
       5. [🔹 **Resumen rápido**](#-resumen-rápido)
   28. [🧩 **Cambiar entre escenas**](#-cambiar-entre-escenas)
       1. [🔹 **Paso 1: Crear el botón en la UI**](#-paso-1-crear-el-botón-en-la-ui)
       2. [🔹 **Paso 2: Crear un Script para manejar la escena**](#-paso-2-crear-un-script-para-manejar-la-escena)
          1. [Explicación](#explicación)
       3. [🔹 **Paso 3: Asignar el script al botón**](#-paso-3-asignar-el-script-al-botón)
       4. [🔹 **Paso 4: Opciones avanzadas**](#-paso-4-opciones-avanzadas)
       5. [🔹 **Tips importantes**](#-tips-importantes)
   29. [🧩 **Capsule Collider en Unity**](#-capsule-collider-en-unity)
       1. [\*\*Para qué sirve](#para-qué-sirve)
       2. [Configuración del Capsule Collider](#configuración-del-capsule-collider)
       3. [Ejemplo visual de propiedades](#ejemplo-visual-de-propiedades)
       4. [Uso con Rigidbody](#uso-con-rigidbody)
       5. [Eventos importantes con Capsule Collider](#eventos-importantes-con-capsule-collider)
       6. [Tips profesionales](#tips-profesionales)
       7. [💡 **Resumen rápido**](#-resumen-rápido-1)
   30. [🧩 **Rigidbody en Unity**](#-rigidbody-en-unity)
       1. [**Agregar un Rigidbody**](#agregar-un-rigidbody)
       2. [**Propiedades principales**](#propiedades-principales)
       3. [**Tipos de movimiento con Rigidbody**](#tipos-de-movimiento-con-rigidbody)
          1. [1. **Movimiento físico**](#1-movimiento-físico)
          2. [2. **Movimiento directo (transform)**](#2-movimiento-directo-transform)
       4. [**Métodos útiles del Rigidbody**](#métodos-útiles-del-rigidbody)
       5. [**Propiedades avanzadas**](#propiedades-avanzadas)
       6. [**Ejemplo práctico de Rigidbody**](#ejemplo-práctico-de-rigidbody)
       7. [Explicación del Ejemplo de Rigidbody](#explicación-del-ejemplo-de-rigidbody)
       8. [**Rigidbody + Colliders**](#rigidbody--colliders)
       9. [**Tips profesionales**](#tips-profesionales-1)
       10. [💡 **Resumen rápido de Rigidbody**](#-resumen-rápido-de-rigidbody)
   31. [indice](#indice)
