# 👾 Avatar Studio: Personajes Literarios Interactivos con IA

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Gradio](https://img.shields.io/badge/Gradio-UI-orange.svg)
![Ollama](https://img.shields.io/badge/Ollama-Local_LLM-black.svg)

Un entorno interactivo basado en Google Colab que permite a los estudiantes dar vida a personajes literarios, figuras históricas o dibujos propios. Utilizando Inteligencia Artificial local y técnicas clásicas de animación por fotogramas, transforma dos imágenes estáticas en un avatar capaz de conversar, pensar y hablar en tiempo real.

Ideal para ferias tecnológicas, incubadoras de proyectos y aulas donde se busque enseñar los fundamentos de la Inteligencia Artificial, la manipulación de video por código y el diseño de *prompts*.

---

## ✨ Características Principales

* **Cerebro IA 100% Local:** Utiliza [Ollama](https://ollama.com/) y el modelo de lenguaje Phi-3 de Microsoft ejecutándose directamente en la máquina virtual, garantizando privacidad y cero costos de API.
* **Animación "Puppeting" (Frame-by-Frame):** Genera la ilusión óptica del habla alternando matemáticamente dos imágenes clave (boca cerrada y abierta) sincronizadas con la duración del audio usando `MoviePy`.
* **Reconocimiento y Síntesis de Voz:** Integra `Whisper` (OpenAI) para entender comandos de voz por micrófono y `Edge-TTS` para dotar al personaje de acentos hispanos fluidos y realistas.
* **Interfaz de Usuario "Creator Studio":** Una interfaz web limpia construida con `Gradio` que separa la configuración del personaje (personalidad, fotos, voz) del área de interacción y chat.

---

## 🚀 Cómo Empezar (Guía de Uso)

Este proyecto está diseñado para ejecutarse sin complicaciones en **Google Colab**, aprovechando sus recursos gratuitos. No necesitas instalar nada en tu computadora local.

### 1. Preparación de Archivos
Antes de iniciar, necesitas crear o descargar dos imágenes de tu personaje (formato `.jpg` o `.png`). Las dimensiones deben ser preferiblemente cuadradas (ej. 500x500px):
1.  Una imagen con la **boca cerrada**.
2.  Una imagen con la **boca abierta** (el resto del rostro debe mantenerse idéntico a la primera).

### 2. Ejecución en Google Colab
1. Sube el cuaderno (`Avatar_Studio.ipynb`) a tu cuenta de Google Colab.
2. Ve al menú superior y selecciona **Entorno de ejecución > Ejecutar todas**.
3. El sistema instalará las dependencias necesarias (esto toma un par de minutos).
4. Al finalizar la última celda, aparecerá un enlace público de Gradio (ej. `https://xxxx-xxxx.gradio.live`). Haz clic para abrir la interfaz web.

### 3. Creando la Magia
Dentro de la interfaz web:
* **Panel Izquierdo:** Sube tus dos imágenes, escribe el *Prompt* (la personalidad que tomará la IA, ej. "Eres Don Quijote...") y elige el acento deseado.
* **Panel Derecho:** Usa el micrófono o el teclado para hablar con tu avatar. ¡El sistema procesará tu mensaje y generará un video de respuesta al instante!

---

## 🧠 Valor Pedagógico y Técnico

Este repositorio no es solo una aplicación de chat, es una herramienta de disección tecnológica. Al revisar el código fuente, los estudiantes pueden aprender:

* **Lógica de Programación Básica:** Uso del operador módulo (`%`) para alternar estados (Pares = Boca Cerrada, Impares = Boca Abierta).
* **Arquitectura de Sistemas:** Cómo conectar múltiples librerías (procesamiento de imágenes con `PIL`, matrices con `NumPy`, renderizado con `MoviePy`).
* **Prompt Engineering:** Entender cómo las instrucciones del sistema (System Prompts) moldean el comportamiento de un Modelo de Lenguaje Grande (LLM).

---

## 🛠️ Tecnologías Utilizadas

* [Google Colab](https://colab.research.google.com/) - Entorno de ejecución en la nube.
* [Gradio](https://gradio.app/) - Framework para la interfaz de usuario web.
* [Ollama](https://ollama.com/) & [Phi-3](https://azure.microsoft.com/en-us/blog/introducing-phi-3-redefining-whats-possible-with-slms/) - Motor y modelo de IA conversacional.
* [MoviePy](https://zulko.github.io/moviepy/) & [Pillow](https://pillow.readthedocs.io/) - Procesamiento y renderizado de video e imágenes.
* [Whisper](https://github.com/openai/whisper) & [Edge-TTS](https://github.com/rany2/edge-tts) - Ecosistema de audio (STT y TTS).

---

## 📄 Licencia

Este proyecto se distribuye con fines educativos. Las librerías de terceros mantienen sus respectivas licencias de código abierto.
