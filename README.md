# Devscan02 (Isaac)

👨🏻‍💻 Soy Isaac — alias Devscan02. Desarrollador y entusiasta de sistemas, scripting y herramientas de bajo nivel. Me centro en automatización, utilidades para sistemas Linux 🐧y proyectos que faciliten instalación, recuperación y análisis de arranque.

## Línea de tiempo

- **2009** — Creación de Batch scripts y aplicaciones en VB.NET. Primeras aplicaciones con GUI en Windows. 🪟
- **2013** — Primer contacto con **C#** (desarrollo con Unity3D). 🎮
- **2016** — Primer contacto con **Linux**. 🐧
- **2020** — Aprendí a usar Linux (nivel: intermedio).
- **2022** — Creación de un instalador en **Bash** para Gentoo en su versión LiveUSB, usando:
  - `unsquashfs` para manipular imágenes squashfs.
  - `zenity` para mostrar diálogos y hacer la instalación más amigable para el usuario.
- **2025** — Desarrollo de **MBRExtractor**, una utilidad para extraer el Master Boot Record desde un dispositivo de almacenamiento (ej. `/dev/sda`) y exportar los primeros 512 bytes a un archivo binario.

## Proyectos destacados

- Instalador Gentoo (LiveUSB)
  - Script en Bash que facilita la preparación del entorno LiveUSB y la instalación.
  - Usa `unsquashfs` para extraer y manipular imágenes squashfs.
  - Integra `zenity` para proporcionar una interfaz gráfica simple (diálogos) durante pasos clave del instalador.

- MBRExtractor
  - Herramienta para extraer el MBR (primeros 512 bytes) de un dispositivo de bloque y guardarlo en un archivo.
  - Uso típico (ejemplo):

```bash
sudo ./MBRExtractor /dev/sda mbr_backup.bin
```

  - Útil para análisis forense básico, copias de seguridad del MBR o diagnóstico de arranque.

## Tecnologías y herramientas

- Sistemas: Linux (uso intermedio/avanzando), Windows
- Lenguajes y scripting: Bash, Batch, VB.NET, C#
- Herramientas y conceptos: squashfs, unsquashfs, zenity, manipulación de dispositivos de bloque, particionado, MBR
- Áreas de interés: automatización, instaladores, utilidades de sistema, recuperación/backup de datos de arranque

## Instrucciones de instalación

### Requisitos generales

- Linux (o WSL con herramientas adecuadas)
- `bash`, `sudo`
- Para el instalador Gentoo: `unsquashfs`, `zenity` y utilidades comunes (`mount`, `dd`, `cp`, etc.)
- Para compilar/utilizar MBRExtractor: herramientas de compilación C/C++ según corresponda (si es binario, revisar el repo del proyecto)

### MBRExtractor (ejemplo)

1. Clonar o descargar el repositorio del proyecto (si existe como repositorio separado).
2. Dar permisos de ejecución al binario o compilar según las instrucciones del repo.
3. Ejecutar con privilegios de superusuario para leer el dispositivo de bloque:

```bash
sudo ./MBRExtractor /dev/sda mbr_backup.bin
```

Advertencia: manipular dispositivos de bloque con `sudo` puede causar pérdida de datos. Asegúrate de especificar el dispositivo correcto.

### Instalador Gentoo (LiveUSB) — notas

- El script usa `unsquashfs` para extraer imágenes squashfs y `zenity` para mostrar diálogos al usuario.
- Requisitos: imagen LiveUSB de Gentoo, `unsquashfs`, `zenity`, permisos adecuados para operar sobre dispositivos y sistemas de archivos.
- El script está pensado para facilitar tareas repetitivas de preparación del LiveUSB y la instalación; revisa y prueba en entornos seguros antes de usar en máquinas de producción.

## Ejemplos de uso

- Extraer MBR a un archivo:

```bash
sudo ./MBRExtractor /dev/sda mbr_sda_2025-01-01.bin
```

- Extraer una imagen squashfs (ejemplo genérico):

```bash
unsquashfs -d destino imagen.squashfs
```

- Mostrar un diálogo simple con zenity desde un script:

```bash
zenity --info --text="Inicio del instalador Gentoo"
```

## Contribuciones

Pull requests y sugerencias son bienvenidas. Abre issues o PRs en los repositorios correspondientes y describe claramente el cambio propuesto. Añade pruebas o instrucciones cuando sea posible.

## Licencia

Licensed under the MIT License. See the LICENSE file for details.

---

# Devscan02 (Isaac) — English

I am Isaac, alias Devscan02. Developer and systems enthusiast focusing on automation, Linux utilities, and low-level tools. I build scripts and small utilities to simplify installation, recovery and boot analysis.

## Timeline

- **2009** — Batch scripts and VB.NET GUI apps on Windows.
- **2013** — First exposure to **C#** (Unity3D).
- **2016** — First contact with **Linux**.
- **2020** — Intermediate Linux usage.
- **2022** — Created a Bash installer for Gentoo LiveUSB using `unsquashfs` and `zenity` to make installation friendlier.
- **2025** — Developed **MBRExtractor**, a utility to export the Master Boot Record (first 512 bytes) from a block device (e.g. `/dev/sda`).

## Highlights

- Gentoo LiveUSB installer: Bash script that uses `unsquashfs` and `zenity` to simplify LiveUSB preparation and installation steps.
- MBRExtractor: Extracts MBR to a binary file for backup or forensic analysis.

## Contact

GitHub: https://github.com/devscan02

---

MIT License

Copyright (c) 2026 Isaac (Devscan02)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
