# 📚 Práctica 1: El entorno de GNU-Linux

> **Plantilla LaTeX para reportes de prácticas**  
> Esta plantilla está lista para usarse. Solo necesitas escribir tu contenido en los lugares indicados.

## 📋 Información del Proyecto

| Campo | Valor |
|-------|-------|
| **Materia** | Cómputo Paralelo |
| **Carrera** | Ingeniería en Inteligencia Artificial |
| **Grupo** | 6BM1 |
| **Escuela** | ESCOM - IPN |
| **Fecha de Entrega** | XX de febrero del 2026 *(actualizar en `config/proyecto.tex`)* |

## 👥 Integrantes del Equipo

1. **Bustillos Cruz Jonatan**
2. **Delgado Lucero Cristian Isaac**
3. **Frem Cortés José Angel**
4. **Luna Gonzales Gabriel Alexis**

---

## 🚀 Inicio Rápido (Para los que tienen prisa)

```bash
# 1. Clonar el repositorio
git clone https://github.com/TakedaTakeishi/p1-paralelo-plataformas-herramientas.git
cd p1-paralelo-plataformas-herramientas

# 2. Crear carpetas para imágenes
mkdir imagenes\instalacion
mkdir imagenes\comandos

# 3. Compilar el documento
latexmk -pdf -outdir=build main.tex

# 4. Ver el PDF generado en: build/main.pdf
```

**¿No tienes LaTeX instalado?** → Ve a la sección [Instalación de LaTeX](#-instalación-de-latex)

---

## 📦 Instalación de LaTeX

### Windows

1. **Descargar MiKTeX:**
   - Ir a https://miktex.org/download
   - Descargar el instalador para Windows
   - Ejecutar e instalar con las opciones predeterminadas

2. **Verificar instalación:**
   ```powershell
   pdflatex --version
   latexmk --version
   ```

### macOS

```bash
# Usando Homebrew
brew install --cask mactex

# O descargar MacTeX desde: https://www.tug.org/mactex/
```

### Linux

```bash
# Ubuntu/Debian
sudo apt-get update
sudo apt-get install texlive-full latexmk

# Fedora
sudo dnf install texlive-scheme-full latexmk

# Arch Linux
sudo pacman -S texlive-most texlive-lang latexmk
```

### Editor recomendado (Opcional)

- **Visual Studio Code** → https://code.visualstudio.com/
  - Instalar extensión: "LaTeX Workshop"
- **TeXstudio** → https://www.texstudio.org/
- **Overleaf** (en línea) → https://www.overleaf.com/

---

## 📂 Guía Paso a Paso

### Paso 1: Obtener el Proyecto

#### Opción A: Clonar con Git (Recomendado)

```bash
git clone https://github.com/TakedaTakeishi/p1-paralelo-plataformas-herramientas.git
cd p1-paralelo-plataformas-herramientas
```

#### Opción B: Descargar ZIP

1. Ve al repositorio: https://github.com/TakedaTakeishi/p1-paralelo-plataformas-herramientas
2. Click en el botón verde "Code"
3. Selecciona "Download ZIP"
4. Descomprime el archivo en tu computadora

### Paso 2: Crear Carpetas para Imágenes

```bash
# Windows (PowerShell)
mkdir imagenes\instalacion
mkdir imagenes\comandos

# macOS/Linux
mkdir -p imagenes/instalacion
mkdir -p imagenes/comandos
```

### Paso 3: Familiarizarte con la Estructura

```
📁 p1-paralelo-plataformas-herramientas/
│
├── 📄 main.tex                    ← Archivo principal (NO TOCAR)
├── 📄 referencias.bib             ← Referencias (si las necesitas)
├── 📄 README.md                   ← Este archivo
│
├── 📁 config/
│   ├── configuracion.tex          ← Configuración de LaTeX (NO TOCAR)
│   └── proyecto.tex               ← ✏️ ACTUALIZAR: fecha de entrega
│
├── 📁 common/
│   ├── portada.tex                ← Portada automática (NO TOCAR)
│   ├── indices.tex                ← Índices automáticos (NO TOCAR)
│   ├── bibliografia.tex           ← Bibliografía (NO TOCAR)
│   └── anexos.tex                 ← Anexos (NO TOCAR)
│
├── 📁 capitulos/                  ← ⭐ AQUÍ ES DONDE TRABAJAS
│   ├── objetivo.tex               ← Ya está completo
│   ├── marco_teorico.tex          ← ✏️ ESCRIBIR aquí
│   ├── instalacion.tex            ← ✏️ ESCRIBIR aquí  
│   ├── comandos.tex               ← ✏️ ESCRIBIR aquí
│   ├── ejercicios.tex             ← ✏️ ESCRIBIR aquí
│   └── conclusiones.tex           ← ✏️ ESCRIBIR aquí
│
├── 📁 imagenes/                   ← 🖼️ GUARDAR capturas aquí
│   ├── logos/                     ← Logos del IPN y ESCOM
│   ├── instalacion/               ← (crear) Capturas de instalación
│   └── comandos/                  ← (crear) Capturas de comandos
│
└── 📁 build/                      ← PDF generado (automático)
    └── main.pdf                   ← Tu documento final
```

### Paso 4: Actualizar la Fecha de Entrega

1. Abre `config/proyecto.tex`
2. Busca la línea:
   ```latex
   \newcommand{\fechaEntrega}{XX de febrero del 2026}
   ```
3. Cambia por la fecha real, ejemplo:
   ```latex
   \newcommand{\fechaEntrega}{28 de febrero del 2026}
   ```

### Paso 5: Encontrar Tu Trabajo Asignado

Cada archivo en `capitulos/` tiene comentarios que empiezan con `% TODO (Tu Nombre):` 

**Ejemplo en `marco_teorico.tex`:**

```latex
% ==========================================
% SECCIÓN 1: Máquinas virtuales
% RESPONSABLE: Bustillos Cruz Jonatan
% ==========================================
\section{Máquinas virtuales}

% TODO (Jonatan): Investiga y escribe sobre máquinas virtuales
% Incluye: definición, tipos, ventajas, desventajas, ejemplos
```

**Busca tu nombre usando:**
- **VS Code:** Ctrl+Shift+F → Buscar "TODO (Tu Nombre)"
- **Windows:** Usa la función de búsqueda en archivos
- **macOS/Linux:** `grep -r "TODO (Tu Nombre)" capitulos/`

### Paso 6: Escribir Tu Contenido

Abre el archivo correspondiente y escribe donde dice `% TODO (Tu Nombre):`

**Ejemplo:**

```latex
\section{Máquinas virtuales}

% TODO (Jonatan): Investiga y escribe sobre máquinas virtuales

% ← BORRA este comentario y escribe tu contenido aquí ↓

Una máquina virtual es un software que emula un sistema de computación 
completo, permitiendo ejecutar un sistema operativo dentro de otro...

\subsection{Tipos de máquinas virtuales}

Existen dos tipos principales de máquinas virtuales:

\begin{itemize}
    \item \textbf{Máquinas virtuales de sistema:} VirtualBox, VMware...
    \item \textbf{Máquinas virtuales de proceso:} JVM, .NET...
\end{itemize}
```

### Paso 7: Agregar Imágenes

1. **Guarda tu captura** en la carpeta correspondiente:
   ```
   imagenes/instalacion/jonatan_paso1.png
   ```

2. **Inserta en LaTeX** donde necesites:
   ```latex
   \begin{figure}[H]
       \centering
       \includegraphics[width=0.8\textwidth]{instalacion/jonatan_paso1.png}
       \caption{Instalación de Ubuntu en VirtualBox - Paso 1}
       \label{fig:jonatan_install1}
   \end{figure}
   ```

**Notas:**
- `width=0.8\textwidth` → La imagen ocupa 80% del ancho (puedes cambiarlo a 0.5, 1.0, etc.)
- La ruta es relativa a `imagenes/` (no pongas `imagenes/` en la ruta)
- **Formatos aceptados:** PNG, JPG, PDF

### Paso 8: Compilar el Documento

#### Opción 1: Línea de Comandos

```bash
# Compilar
latexmk -pdf -outdir=build main.tex

# Limpiar archivos temporales
latexmk -C -outdir=build
```

#### Opción 2: Visual Studio Code con LaTeX Workshop

1. Abre `main.tex`
2. Presiona `Ctrl+Alt+B` (o click en ✓ Build LaTeX project)
3. El PDF se generará automáticamente

#### Opción 3: TeXstudio

1. Abre `main.tex`
2. Tools → Build & View (o presiona F5)

### Paso 9: Ver el Documento Generado

El PDF se genera en: `build/main.pdf`

---

## 📝 Distribución de Tareas por Integrante

### 🔵 Bustillos Cruz Jonatan

<details>
<summary><b>Ver tareas asignadas (click para expandir)</b></summary>

#### Marco Teórico (5 temas):
1. Máquinas virtuales
2. Distribuciones de GNU-Linux
3. Requisitos de instalación del sistema operativo GNU-Linux
4. Estadísticas de uso del sistema operativo GNU-Linux en el mundo
5. Escritorios GNOME y KDE

#### Comandos (10):
`ps`, `more`, `time`, `du`, `ps -fea`, `less`, `uname`, `pstree`, `man`, `mkdir`

#### Otros:
- Instalación personal de GNU-Linux (con capturas)
- Conclusión personal
- Crear y gestionar el repositorio

**Archivo principal:** `capitulos/marco_teorico.tex`, `capitulos/comandos.tex`

</details>

---

### 🟢 Delgado Lucero Cristian Isaac

<details>
<summary><b>Ver tareas asignadas (click para expandir)</b></summary>

#### Marco Teórico (6 temas):
1. Entornos Command Line Interface y Graphical User Interface
2. Terminal de GNU-Linux
3. Tipos de usuario en GNU-Linux
4. Rutas relativas y absolutas
5. Redireccionamiento
6. Clasificación de los comandos en GNU-Linux

#### Comandos (10):
`cal`, `clear`, `apt`, `rm`, `date`, `ifconfig`, `exit`, `mv`, `echo`, `df`

#### Otros:
- Instalación personal de GNU-Linux (con capturas)
- Conclusión personal

**Archivo principal:** `capitulos/marco_teorico.tex`, `capitulos/comandos.tex`

</details>

---

### 🟡 Frem Cortés José Angel

<details>
<summary><b>Ver tareas asignadas (click para expandir)</b></summary>

#### Marco Teórico (2 temas):
1. Variables de entorno
2. Comandos de GNU-Linux mostrados en la tabla 1 (descripción general)

#### Comandos (9):
`w`, `kill -l -9`, `cat`, `pico`, `who`, `trap -l`, `fg`, `nano`, `bash`

#### Ejercicios Prácticos (4):
1. **Rutas:** 3 ejemplos de rutas absolutas + 3 de rutas relativas
2. **Borrado:** 3 ejemplos usando `rm` con comodines `*` y `?`
3. **Redireccionamiento:** 2 ejemplos con `>` y `>>`
4. **Instalación CLI:** Instalar software por línea de comandos (ej: gimp)

#### Otros:
- Instalación personal de GNU-Linux (con capturas)
- Conclusión personal

**Archivos principales:** `capitulos/marco_teorico.tex`, `capitulos/comandos.tex`, `capitulos/ejercicios.tex`

</details>

---

### 🟣 Luna Gonzales Gabriel Alexis

<details>
<summary><b>Ver tareas asignadas (click para expandir)</b></summary>

#### Comandos (9):
`pwd`, `cd`, `vi`, `wc`, `su`, `ls`, `apt-get`, `sudo`, `ls -la`

#### Ejercicios Prácticos (5):
1. **Instalación GUI:** Instalar software usando entorno gráfico
2. **Jerarquía:** 5 ejemplos de mover/copiar archivos y directorios
3. **Usuarios:** Agregar usuario, verificar, entrar en sesión, borrar
4. **Hola Mundo con nano:** Crear, compilar y ejecutar programa en C
5. **Hola Mundo con gedit:** Crear, compilar y ejecutar programa en C

#### Otros:
- Instalación personal de GNU-Linux (con capturas)
- Conclusión personal

**Archivos principales:** `capitulos/comandos.tex`, `capitulos/ejercicios.tex`

</details>

---

## 💡 Consejos y Buenas Prácticas

### ✅ Hacer (DO)

- ✅ **Guarda con frecuencia:** Presiona `Ctrl+S` o `Cmd+S` constantemente
- ✅ **Compila frecuentemente:** Compila cada vez que termines una sección para detectar errores
- ✅ **Nombres de archivos:** Usa nombres descriptivos sin espacios
  - ✅ Correcto: `jonatan_instalacion_paso1.png`
  - ❌ Incorrecto: `Captura de pantalla 2026-02-15.png`
- ✅ **Capturas claras:** Asegúrate de que el texto sea legible
- ✅ **Describe las imágenes:** Usa captions descriptivos
- ✅ **Guarda tus cambios en Git:**
  ```bash
  git add .
  git commit -m "Agregué mi sección de máquinas virtuales"
  git push
  ```

### ❌ Evitar (DON'T)

- ❌ **NO edites** `main.tex` (a menos que sepas lo que haces)
- ❌ **NO edites** archivos en `common/` o `config/configuracion.tex`
- ❌ **NO uses** acentos o ñ en nombres de archivos de imágenes
- ❌ **NO subas** archivos de la carpeta `build/` al repositorio
- ❌ **NO copies y pegues** directamente desde Word (puede causar errores)- ❌ **NO uses** comandos LaTeX complejos que no entiendas

### 📐 Formato de Texto en LaTeX

```latex
% Texto en negritas
\textbf{Este texto está en negritas}

% Texto en cursiva
\textit{Este texto está en cursiva}

% Código o comandos
El comando \texttt{ls -la} lista todos los archivos

% Listas con viñetas
\begin{itemize}
    \item Primer elemento
    \item Segundo elemento
    \item Tercer elemento
\end{itemize}

% Listas numeradas
\begin{enumerate}
    \item Primer paso
    \item Segundo paso
    \item Tercer paso
\end{enumerate}

% Bloques de código
\begin{lstlisting}[language=bash]
sudo apt-get update
sudo apt-get install gimp
\end{lstlisting}

% Citas
\begin{quote}
Este es un texto citado.
\end{quote}
```

---

## 🔍 Preguntas Frecuentes (FAQ)

### ¿Cómo sé qué tengo que hacer?

Busca tu nombre en los archivos de `capitulos/`. Verás comentarios como:
```latex
% TODO (Tu Nombre): Descripción de la tarea
```

### ¿Puedo usar Overleaf en lugar de instalar LaTeX?

Sí, puedes:
1. Crear una cuenta en https://overleaf.com/
2. Crear nuevo proyecto → Upload Project
3. Sube el archivo ZIP del repositorio
4. Trabaja en línea

**Nota:** Tendrás que descargar y subir los cambios manualmente si trabajas en equipo.

### ¿Cómo actualizo mi copia del repositorio?

```bash
# Antes de empezar a trabajar
git pull origin main

# Después de hacer cambios
git add .
git commit -m "Descripción de lo que hice"
git push origin main
```

### Error: "File not found" al compilar

**Problema:** LaTeX no encuentra una imagen

**Solución:**
1. Verifica que la imagen esté en `imagenes/`
2. Verifica que el nombre del archivo sea exacto (mayúsculas/minúsculas)
3. No incluyas `imagenes/` en la ruta:
   ```latex
   % ✅ Correcto
   \includegraphics{comandos/ejemplo.png}
   
   % ❌ Incorrecto  
   \includegraphics{imagenes/comandos/ejemplo.png}
   ```

### Error: "Undefined control sequence"

**Problema:** Usaste un comando LaTeX que no existe o está mal escrito

**Solución:**
1. Revisa el error en el log (te dice la línea exacta)
2. Verifica la ortografía del comando
3. Asegúrate de cerrar todos los `{` con `}`

### Mi PDF se ve diferente al de mis compañeros

Es normal si están trabajando en paralelo. El PDF final se verá completo cuando todos hayan terminado.

### ¿Cómo inserto código de C en el documento?

```latex
\begin{lstlisting}[language=C]
#include <stdio.h>

int main() {
    printf("Hola Mundo\n");
    return 0;
}
\end{lstlisting}
```

### ¿Puedo cambiar el tamaño de las letras en la portada?

Sí, revisa los comentarios en `common/portada.tex`. Hay instrucciones sobre cómo cambiar cada tamaño.

---

## ✅ Checklist de Progreso

Marca con una `x` cuando completes cada tarea:

### Preparación
- [ ] LaTeX instalado y funcionando
- [ ] Repositorio clonado/descargado
- [ ] Carpetas de imágenes creadas
- [ ] Documento compila correctamente (primera vez)
- [ ] Fecha de entrega actualizada

### Contenido (Todos)
- [ ] Instalación de GNU-Linux documentada con capturas
- [ ] Conclusión personal escrita

### Marco Teórico
- [ ] Sección 1-5 (Jonatan)
- [ ] Sección 6-11 (Cristian)
- [ ] Sección 12-13 (José Angel)

### Comandos
- [ ] 10 comandos (Jonatan)
- [ ] 10 comandos (Cristian)
- [ ] 9 comandos (José Angel)
- [ ] 9 comandos (Gabriel)

### Ejercicios Prácticos
- [ ] Rutas, borrado, redireccionamiento, instalación CLI (José Angel)
- [ ] Instalación GUI, jerarquía, usuarios, Hola Mundo x2 (Gabriel)

### Finalización
- [ ] Todas las imágenes incluidas correctamente
- [ ] PDF compila sin errores
- [ ] Revisión ortográfica
- [ ] Revisión de formato
- [ ] PDF final revisado por todo el equipo

---

## 🔧 Solución de Problemas Comunes

### Problema: "pdflatex: command not found"

**Causa:** LaTeX no está instalado o no está en el PATH

**Solución:**
1. Instala LaTeX siguiendo la sección [Instalación de LaTeX](#-instalación-de-latex)
2. Reinicia la terminal/PowerShell
3. Verifica con: `pdflatex --version`

### Problema: "Cannot write file 'build/main.aux'"

**Causa:** La carpeta `build/` está corrupta o bloqueada

**Solución:**
```bash
# Windows
Remove-Item -Recurse -Force build
New-Item -ItemType Directory -Name build
latexmk -pdf -outdir=build main.tex

# macOS/Linux
rm -rf build
mkdir build
latexmk -pdf -outdir=build main.tex
```

### Problema: Caracteres con acentos se ven mal

**Causa:** Archivo no está en UTF-8

**Solución:**
- **VS Code:** Click en la esquina inferior derecha donde dice "UTF-8" o la codificación actual → "Save with Encoding" → UTF-8
- **Notepad++:** Menu Encoding → Convert to UTF-8
- **TeXstudio:** Edit → Set Encoding → UTF-8

### Problema: La imagen se sale de la página

**Solución:**
Reduce el `width`:
```latex
% En lugar de:
\includegraphics[width=1.2\textwidth]{mi_imagen.png}

% Usa:
\includegraphics[width=0.8\textwidth]{mi_imagen.png}
```

### Problema: Git dice "merge conflict"

**Causa:** Dos personas editaron el mismo archivo

**Solución:**
1. Abre el archivo con conflicto
2. Busca las secciones marcadas con `<<<<<<<`, `=======`, `>>>>>>>`
3. Decide qué versión mantener o combina ambas
4. Elimina los marcadores de conflicto
5. Guarda y haz commit:
   ```bash
   git add archivo_resuelto.tex
   git commit -m "Resuelto conflicto en archivo_resuelto.tex"
   git push
   ```

### Problema: "Overfull \hbox" o "Underfull \hbox"

**Causa:** LaTeX no puede ajustar el texto correctamente

**Solución:**
- Estos son **warnings**, no errores. El PDF se genera de todos modos
- Generalmente se pueden ignorar
- Si te molestan, intenta reformular el texto o agregar `\-` para sugerir dónde dividir palabras

### Problema: Las references/citas no aparecen

**Causa:** Necesitas compilar varias veces o ejecutar Biber

**Solución:**
```bash
latexmk -pdf -outdir=build main.tex
```
El comando `latexmk` ejecuta automáticamente todas las compilaciones necesarias.

---

## 📚 Recursos Adicionales

### Tutoriales de LaTeX

- **Overleaf Learn:** https://www.overleaf.com/learn
- **LaTeX Wikibook:** https://en.wikibooks.org/wiki/LaTeX
- **Tutorial en español:** https://ondiz.github.io/cursoLatex/

### Ayuda con Comandos

- **Páginas de manual de Linux:** https://man7.org/linux/man-pages/
- **Explain Shell:** https://explainshell.com/ (explica comandos bash)

### Git y GitHub

- **Git Handbook:** https://guides.github.com/introduction/git-handbook/
- **GitHub Desktop:** https://desktop.github.com/ (interfaz gráfica para Git)

### Editores de LaTeX

- **Visual Studio Code:** https://code.visualstudio.com/
  - Extensión: "LaTeX Workshop" by James Yu
- **TeXstudio:** https://www.texstudio.org/
- **Overleaf:** https://www.overleaf.com/ (en línea, no requiere instalación)

---

## 📞 Soporte y Contacto

### ¿Tienes dudas sobre tu tarea específica?

1. Revisa este README completo
2. Busca en la sección de [FAQ](#-preguntas-frecuentes-faq)
3. Pregunta en el grupo de WhatsApp del equipo

### ¿Encontraste un error en la plantilla?

Abre un "Issue" en GitHub:
1. Ve a https://github.com/TakedaTakeishi/p1-paralelo-plataformas-herramientas/issues
2. Click en "New Issue"
3. Describe el problema con detalles

---

## 📄 Licencia y Créditos

Este proyecto es una plantilla educativa para la práctica de la materia de Cómputo Paralelo.

**Desarrollado por:** Equipo 6BM1  
**Escuela:** ESCOM - Instituto Politécnico Nacional  
**Ciclo:** 7º Semestre - 2026  

---

## 🎯 Objetivos de Aprendizaje

Al completar esta práctica, habrás aprendido:

- ✅ Instalar y configurar GNU-Linux
- ✅ Usar comandos básicos y avanzados de la terminal
- ✅ Gestionar archivos y directorios
- ✅ Administrar usuarios y permisos
- ✅ Compilar programas en C desde la terminal
- ✅ Documentar procesos técnicos profesionalmente
- ✅ Trabajar en equipo usando Git/GitHub
- ✅ Crear documentos técnicos con LaTeX

---

## 🚀 ¡Comienza Ahora!

1. **Instala LaTeX** → [Ver instrucciones](#-instalación-de-latex)
2. **Clona el repositorio** → [Inicio Rápido](#-inicio-rápido-para-los-que-tienen-prisa)
3. **Busca tus tareas** → [Distribución de Tareas](#-distribución-de-tareas-por-integrante)
4. **Escribe tu contenido** → [Guía Paso a Paso](#-guía-paso-a-paso)
5. **Compila y revisa** → `latexmk -pdf -outdir=build main.tex`

---

**¿Listo para empezar? ¡Éxito en la práctica! 🚀**

*Última actualización: 15 de febrero de 2026*
