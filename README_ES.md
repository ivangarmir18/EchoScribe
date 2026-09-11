<div align="center">

# EchoScribe AI Studio (Español)

### **Estudio Integral de Transcripción por Voz y Generación de Contenido para Windows**
*Transcripción rápida con Whisper en la nube GPU, generación de titulares y resúmenes con IA, descarga directa de medios (MP3/MP4) y formateo inteligente de subtítulos para CapCut, Premiere y DaVinci.*

[![Web Oficial](https://img.shields.io/badge/Web_Oficial-echoscribe.es-6366f1?style=for-the-badge&logo=google-chrome&logoColor=white)](https://www.echoscribe.es)
[![Descargar Instalador](https://img.shields.io/badge/Descargar_Instalador-v1.3.3-10b981?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/ivangarmir18/EchoScribe/releases)
[![Informe VirusTotal](https://img.shields.io/badge/VirusTotal-Verificado_Limpio-brightgreen?style=for-the-badge&logo=virustotal&logoColor=white)](https://www.virustotal.com/gui/file/ec0517c1cc365f2dfb43d8715e7aaaa3b8cf6583c63ef8b121f6107fc163f55d/detection)
[![GitHub release](https://img.shields.io/github/v/release/ivangarmir18/EchoScribe?style=for-the-badge&color=blue)](https://github.com/ivangarmir18/EchoScribe/releases)
[![Licencia: MIT](https://img.shields.io/badge/Licencia-MIT-yellow.svg?style=for-the-badge)](LICENSE)

<br/>

**[English](README.md)** • **[Español](README_ES.md)** • **[Arquitectura Técnica](docs/ARCHITECTURE.md)** • **[Benchmarks](docs/BENCHMARKS.md)** • **[Descargar Instalador](https://github.com/ivangarmir18/EchoScribe/releases)**

<br/>

> **"Convierte cualquier audio, vídeo o enlace de streaming en transcripciones exactas, resúmenes con IA y subtítulos sincronizados para tus vídeos en cuestión de segundos."**

</div>

---

## Galería de la Aplicación

<div align="center">

### Panel Principal de EchoScribe AI Studio
![Panel Principal de EchoScribe AI Studio](docs/img/1.png)
*Interfaz de escritorio moderna con ingesta de enlaces, selector de idioma, transcripción rápida con IA y descarga directa.*

<br/>

| Recortador de Audio Interactivo | Ajustes y Perfiles de Subtítulos | Centro de Exportación Multiformato |
| :---: | :---: | :---: |
| ![Recortador de Audio](docs/img/2.png) | ![Ajustes de Subtítulos](docs/img/3.png) | ![Modal de Exportación](docs/img/4.png) |
| *Selector de intervalo visual (0-30 min, atajo 1er minuto)* | *Perfiles ergonómicos (TikTok/Reels, YouTube, Cine)* | *Exportación en 1 clic a TXT, Word, PDF, Markdown y SRT* |

</div>

---

## ¿Qué es EchoScribe AI Studio?

**EchoScribe AI Studio** es una aplicación de escritorio nativa para Windows pensada para creadores de contenido, editores de vídeo, periodistas, estudiantes y profesionales que necesitan transcripciones rápidas y precisas sin pelearse con scripts de Python, drivers de CUDA ni webs lentas con suscripciones abusivas.

### ¿Qué hace única a la aplicación?

1. **Ingesta Universal y Descargador de Medios**:
   - Pega enlaces directos de **YouTube, X (Twitter) o Twitch**, o arrastra archivos locales (**MP3, MP4, WAV, MKV, M4A, FLAC**).
   - Botones dedicados de descarga directa para obtener el audio en **MP3** o el vídeo en **MP4** con un solo clic.

2. **Recortador de Audio Interactivo (Trimmer)**:
   - Barra visual de rango para transcribir únicamente el fragmento que necesitas (por ejemplo, el primer minuto o un intervalo específico de tiempo), ahorrando minutos de tu plan.

3. **Dos Modos de Procesamiento**:
   - **⚡ Transcripción Rápida (~50–70s)**: Inferencia directa con Whisper Ultra en clúster GPU en la nube para obtener el texto literal al instante.
   - **⚡ Transcribir + Análisis IA (~80–120s)**: Transcripción fonética combinada con búsqueda contextual para generar automáticamente **Titulares** y un **Resumen Ejecutivo** estructurado.

4. **Subtítulos Inteligentes para Premiere, CapCut y DaVinci (.SRT)**:
   - Ajuste de longitud de subtítulo según la plataforma de destino:
     - **Corto (15–26 car.)**: Pensado para TikTok, Instagram Reels y YouTube Shorts.
     - **Medio (27–40 car.)**: Cadencia natural para vídeos estándar de YouTube y divulgación.
     - **Largo (41–55 car.)**: Estándar para cine, entrevistas y documentales.
   - Algoritmo que evita líneas huérfanas y cortes antiestéticos en mitad de palabras clave.

5. **Exportación Multiformato en 1 Clic**:
   - **Texto Plano (.TXT)**: Ligero y universal.
   - **Documento Word (.DOC)**: Maquetado con títulos y estilos para Microsoft Word.
   - **Documento PDF (.PDF)**: Paginado y listo para imprimir o enviar.
   - **Markdown (.MD)**: Formato óptimo para Notion, Obsidian o blogs técnicos.
   - **Subtítulos (.SRT)**: Bloques sincronizados listos para soltar en la línea de tiempo de tu editor de vídeo.

6. **Experiencia Nativa en Windows**:
   - Desarrollado sobre Microsoft Edge WebView2 (Chromium nativo).
   - Inicio ultrarrápido (< 1.2s), mínimo consumo de memoria RAM (< 180MB), tema oscuro/claro y control de escala/zoom (90%, 100%, 112%).

---

## Estructura del Repositorio: Código Algorítmico + Releases

Este repositorio cumple dos funciones claras:
1. **Núcleo Algorítmico Open-Source (`quickstart_demo.py`)**: Contiene el código fuente en Python de los algoritmos clave de EchoScribe: el limpiador de bucles de alucinación de Whisper y el particionador semántico de subtítulos sin palabras huérfanas. Cualquiera puede probarlo o integrarlo en sus proyectos.
2. **Distribución de la Aplicación de Escritorio**: Punto de encuentro oficial para el instalador compilado de Windows (`EchoScribe_Setup.exe`), notas de versión, auditoría de seguridad en VirusTotal y documentación técnica de la arquitectura.

---

## Cómo Probar la Demo Algorítmica en Local

Puedes probar el núcleo algorítmico en tu máquina en menos de un minuto sin configurar GPUs ni claves API:

```bash
# 1. Clonar el repositorio
git clone https://github.com/ivangarmir18/EchoScribe.git
cd EchoScribe

# 2. Ejecutar la demo
python quickstart_demo.py

# 3. Ejecutar los tests automáticos
python -m pytest test_quickstart.py
```

---

## Descarga e Instalación en Windows

Para utilizar la aplicación completa con interfaz gráfica:

1. Descarga el instalador **`EchoScribe_Setup.exe` (v1.3.3)** desde [**echoscribe.es**](https://www.echoscribe.es) o desde [**Releases de GitHub**](https://github.com/ivangarmir18/EchoScribe/releases).
2. Comprueba el [**Informe de Seguridad en VirusTotal**](https://www.virustotal.com/gui/file/ec0517c1cc365f2dfb43d8715e7aaaa3b8cf6583c63ef8b121f6107fc163f55d/detection).
3. Ejecuta el instalador. Añadirá un acceso directo en tu escritorio y un desinstalador limpio en el panel de control.

---

## Documentación Técnica

- [**docs/ARCHITECTURE.md**](docs/ARCHITECTURE.md): Diagramas de flujo de datos, gestor de descargas yt-dlp y diseño de infraestructura GPU.
- [**docs/BENCHMARKS.md**](docs/BENCHMARKS.md): Pruebas de velocidad, factores de tiempo real (RTF) y tasa de error fonético.

---

## Licencia

Distribuido bajo la Licencia MIT. Consulta [LICENSE](LICENSE) para más detalles.

Desarrollado por [Iván García Miranda](https://www.echoscribe.es/sobre-mi).
