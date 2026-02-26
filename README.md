# 🛡️ Curso de Desarrollo Seguro en C/C++

¡Bienvenido al curso! Este repositorio contiene todo lo necesario para configurar tu entorno de desarrollo en menos de un minuto utilizando la nube. No necesitas instalar compiladores ni herramientas pesadas en tu ordenador.

## 🚀 Configuración del Entorno (En 3 pasos)

Para que todos tengamos exactamente las mismas herramientas y errores, utilizaremos **GitHub Codespaces**.

1. Haz clic en el botón verde **"<> Code"** (arriba a la derecha).
2. Selecciona la pestaña **"Codespaces"**.
3. Haz clic en el botón azul **"Create codespace on main"**.

*Se abrirá una pestaña nueva con un editor VS Code en tu navegador. Espera unos segundos a que termine de configurarse.*

---

## 🛠️ Herramientas de Seguridad Incluidas

Este entorno viene pre-configurado con las siguientes herramientas esenciales para el desarrollo seguro:

* **Compilador:** `gcc` / `g++` (Ubuntu 22.04).
* **Análisis Estático:** * `flawfinder`: Busca funciones vulnerables (como `strcpy` o `gets`).
    * `cppcheck`: Detecta errores de lógica y desbordamientos.
    * `SonarLint`: Extensión de VS Code que te avisa de fallos mientras escribes.
* **Análisis Dinámico:**
    * `Valgrind`: Para detectar fugas de memoria y accesos inválidos.
    * `GDB`: Depurador para analizar el estado de la pila (stack).

---

## 💻 Comandos Útiles para Clase

### 1. Compilación con Protecciones (Modo Seguro)
```bash
g++ -Wall -Wextra -O2 -fsanitize=address programa.cpp -o programa
