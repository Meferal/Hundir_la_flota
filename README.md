<div align="center">

![portada](./img/hundir-la-flota-juego-de-mesa.jpg)

# 🚢 Hundir la Flota en Python

![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.26+-green?logo=numpy)
![Game](https://img.shields.io/badge/Genre-CLI%20Game-orange)
![Platform](https://img.shields.io/badge/Platform-Terminal-lightgrey)
![License](https://img.shields.io/badge/License-MIT-yellow)

**Juego completo de Hundir la Flota ejecutable por terminal con IA,
generación procedural de barcos y visualización dinámica.**

[Ver Documentación](./docs/) • [Reportar
Bug](https://github.com/Meferal/Hundir_la_flota/issues/new?labels=bug) •
[Solicitar
Feature](https://github.com/Meferal/Hundir_la_flota/issues/new?labels=enhancement)

</div>

------------------------------------------------------------------------

# 📖 Descripción

Este proyecto implementa una versión completa del clásico **Hundir la
Flota** (Battleship) ejecutable por terminal. El sistema incluye:

-   Generación aleatoria y validada de barcos sin solapamientos\
-   Gestión de turnos jugador vs IA\
-   IA que evita disparar dos veces a la misma casilla\
-   Visualización de tableros con numeración\
-   Estado del juego en tiempo real\
-   Arquitectura modular separada en `main.py` y `utils.py`

Procesos como la creación de barcos, ataques, comprobaciones y control
del flujo del juego se encuentran completamente encapsulados para
permitir escalabilidad.

------------------------------------------------------------------------

# 🎯 Objetivos del Proyecto

### ✔ Crear un motor funcional del juego Hundir la Flota

Incluyendo lógica de ataque, impactos, agua, hundimientos y condiciones
de victoria.

### ✔ Implementar IA simple, autónoma y no repetitiva

Skynet dispara únicamente a coordenadas no atacadas anteriormente,
generando partidas consistentes.

### ✔ Desarrollar un sistema robusto de generación de barcos

Totalmente aleatorio, validado y sin solapamientos.

### ✔ Optimizar la visualización en terminal

Se emplea NumPy para una representación clara y numerada del tablero.

### ✔ Arquitectura modular profesional

-   `utils.py`: lógica principal del juego\
-   `main.py`: flujo de ejecución, bucle de partida, interacción con el
    usuario

------------------------------------------------------------------------

# 🗂️ Estructura del Proyecto

    📦 Hundir_La_Flota
    │
    ├── main.py               # Flujo completo del juego y ejecución por terminal
    ├── utils.py              # Funciones: tableros, barcos, disparos, lógica interna
    ├── README.md             # Documentación del proyecto
    └── docs/
        └── img/              # Capturas ASCII (opcional)

------------------------------------------------------------------------

# ⚙️ Instalación y Requisitos

### 🔹 Requisitos

-   Python **3.11+**
-   NumPy **1.26+**

### 🔹 Instalación

    pip install numpy

### 🔹 Ejecución

    python main.py

------------------------------------------------------------------------

# 🧠 Arquitectura del Juego

### 1. **Generación del tablero**

-   Arrays NumPy de 10×10\
-   Representación de agua con `_`\
-   Tablero visual numerado para el usuario

### 2. **Generación de barcos**

Lista por defecto: - 1 barco de eslora 4\
- 2 barcos de eslora 3\
- 3 barcos de eslora 2

Características: - Orientación aleatoria (horizontal/vertical)\
- Sentido aleatorio (izquierda/derecha, arriba/abajo)\
- Validación estricta para evitar solapamientos

### 3. **Lógica de ataque**

-   `Tocado`: `"X"`\
-   `Agua`: `"A"`

### 4. **IA (Skynet)**

-   Ataca de forma completamente aleatoria\
-   Nunca dispara dos veces a la misma casilla (registro
    `coord_skynet`)\
-   Ataca hasta obtener **Agua**

### 5. **Condición de victoria**

-   Uno de los dos jugadores pierde todos los barcos\
-   O se cumplen 10 turnos → empate por agotamiento

------------------------------------------------------------------------

# 🖥️ Capturas ASCII del Juego

### 🔹 Tablero del jugador

       / 0 1 2 3 4 5 6 7 8 9
    0  _ _ _ O O O O _ _ _
    1  _ _ _ _ _ _ _ _ _ _
    2  _ _ _ _ _ _ _ _ _ _
    3  _ _ _ _ _ _ _ _ _ _
    4  _ _ _ O O O _ _ _ _
    5  _ _ _ _ _ _ _ _ _ _
    6  _ _ _ _ _ _ _ _ _ _
    7  _ _ _ _ _ _ _ _ _ _
    8  O _ _ _ _ _ _ _ _ _
    9  O _ _ _ _ _ _ _ _ _

### 🔹 Tablero enemigo (oculto)

       / 0 1 2 3 4 5 6 7 8 9
    0  _ _ _ _ _ _ _ _ _ _
    1  _ _ A A _ _ _ _ _ _
    2  _ _ _ _ _ _ _ _ _ _
    3  _ _ _ _ _ _ _ _ _ _
    4  _ _ _ _ _ _ _ _ _ _
    5  _ _ _ _ X X _ _ _ _
    6  _ _ _ _ _ _ _ _ _ _
    7  _ _ _ _ _ _ _ _ _ _
    8  _ _ _ _ _ _ _ _ _ _
    9  _ _ _ _ _ _ _ _ _ _

### 🔹 Mensajes de batalla

    Turno 3 de 10
    Introduce la casilla a la que vas a disparar (fila,columna): 5,4
    Tocado
    El enemigo ha atacado las coordenadas: (8, 1)
    Agua

------------------------------------------------------------------------

# 🔧 Funcionalidades del Juego

  Funcionalidad                        Estado
  ----------------------------------- --------
  Generación procedural de barcos        ✅
  Validación anti-solapamientos          ✅
  Ataque con IA                          ✅
  Sistema de turnos                      ✅
  Tablero numerado                       ✅
  Representación de agua y tocado        ✅
  Finalización por victoria/empate       ✅
  Ejecución completa desde terminal      ✅

------------------------------------------------------------------------

# 🧑‍💻 Autor

**Álvaro Medina Fernández**\
[LinkedIn](http://www.linkedin.com/in/álvaro-medinafernández) \|
[GitHub](https://github.com/Meferal)

------------------------------------------------------------------------

# 📜 Licencia

Proyecto distribuido bajo licencia **MIT**.
