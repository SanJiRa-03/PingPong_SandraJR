# 🏓 Ping Pong en Unreal Engine 5

Pong completo desarrollado con **Unreal Engine 5** y **Blueprints**. Se puede jugar contra la IA o contra otra persona, y gana quien llegue primero a 15 puntos. 🎮

📌 **Contexto:** proyecto individual de la asignatura *Introducción a la Programación de Videojuegos y Entornos Virtuales* (UDIT, curso 2026/2027). La memoria del proyecto la redacté yo y está en la carpeta `docs/`.

## 🚀 Funcionalidades

* 🤖 **Dos modos:** Jugador vs IA y Jugador vs Jugador.
* ⚽ **Pelota con físicas:** rebota en las palas y en los muros, y gana velocidad con los golpes.
* 🥅 **Goles:** triggers detrás de cada pala que suman un punto al rival.
* 💡 **Marcador parpadeante:** tras cada gol parpadea 5 segundos y sale una pelota nueva.
* 🏁 **Fin de partida:** a los 15 puntos aparece el ganador, con las opciones de repetir o volver al menú.
* 💾 **Guardado:** las victorias acumuladas se conservan entre sesiones, con un registro por modo.
* 🎥 **Cámara fija ortográfica** que recrea el aspecto plano del Pong original.

## 🧠 Cómo funciona por dentro

| 🧩 Apartado | 🎯 Cómo está hecho |
|---|---|
| 🏓 Palas y controles | Un Blueprint por pala y **Enhanced Input** (acción `Mover` y contexto `PingPongControles`). |
| ⚽ Pelota y rebotes | Actor con simulación de físicas y un *Physical Material* de alta restitución y baja fricción. |
| 🥅 Detección de goles | Volúmenes *trigger* con eventos de solapamiento. |
| 🖼️ Marcador | Widget **UMG** con la puntuación de cada jugador. |
| 🎬 Escenas | Menú principal y un nivel por modo de juego. |
| 💾 Persistencia | Clase `SaveGame` con un *slot* por modo. |

## 🛠️ Tecnologías y conceptos

* 🧱 **Blueprints** como lenguaje de programación visual.
* ⌨️ **Enhanced Input** para gestionar las teclas.
* ⚙️ **Físicas y colisiones** con *Collision Presets*.
* 🖼️ **UMG** para la interfaz.
* 💾 **Save Game** para guardar datos entre sesiones.

## 🗂️ Cómo está organizado

| 📁 Carpeta | 🎯 Contenido |
|---|---|
| `Content/Blueprints` | Palas, pelota, spawner, goles, puntuación y guardado. |
| `Content/Input` | Acción `Mover` y contexto de mapeo. |
| `Content/Mapas` | Menú principal y niveles de partida. |
| `Content/Material` | Materiales neón. |
| `Content/Fuentes` y `Content/Sonidos` | Tipografías y efecto de sonido. |

## ▶️ Cómo jugarlo

1. Descarga el build para **Windows** desde su [página en itch.io](https://sandra-jimenez-ramiro.itch.io/ping-pong).
2. Descomprime el archivo `.zip`.
3. Ejecuta el `.exe` y elige **Jugador vs Jugador** o **Jugador vs IA**.

## ▶️ Cómo abrirlo

1. Instala **Unreal Engine 5.8** desde el Epic Games Launcher.
2. Descarga este repositorio.
3. Abre `PingPong_SandraJR.uproject` y espera a que compile los shaders.
4. Abre el mapa `MenúPrincipal` y pulsa **Play**.

## 📎 Documentación

La carpeta [`docs/`](docs/) incluye la **memoria** del proyecto: descripción técnica, diario de desarrollo y pruebas realizadas.

## 🙌 Créditos

* 📺 Basado en el tutorial *How To Make Pong In Unreal Engine 5 Blueprint Tutorial*, de Unreal University. Son aportaciones propias el modo contra la IA, el parpadeo del marcador, el límite de 15 puntos, los menús y el guardado.

---
🎓 *Práctica académica para trabajar Blueprints, físicas, interfaz, escenas y guardado de partidas en Unreal Engine.*
