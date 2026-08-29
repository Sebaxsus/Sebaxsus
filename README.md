<style>
  h2 {
    padding-bottom: 24px;
    text-align: center;
    margin-bottom: 2rem;
  }

  h3 {
    text-indent: 2ch;
  }
</style>

<h2>Juan Sebastián García Redondo</h2>

###

<h2>Sobre mí / About Me</h2>

<h3>ESPAÑOL 🇪🇸</h3>
<p>
Estudiante de Ingeniería de Software, buscando mi <strong>práctica profesional</strong> (último requisito para graduarme). A la par de mi formación universitaria, llevo <strong>4 años construyendo proyectos de forma autodidacta</strong>: bots, automatizaciones, sistemas full-stack conectados a hardware embebido y, más recientemente, aplicaciones de <strong>IA local</strong> (transcripción de audio + RAG corriendo por completo en mi propia máquina, sin depender de la nube).

Me interesa especialmente diseñar arquitecturas robustas (Domain-Driven Design, sincronización offline-first, sistemas "Server as the Source of Truth") y software que conversa directamente con hardware (ESP32, Arduino) o con modelos de IA ejecutándose de forma local.

Mi motor principal es solucionar problemas de la vida cotidiana con el desarrollo de herramientas por medio del software y hardware.
</p>
<hr/>
<h3>ENGLISH 🇺🇸</h3>
<p>
Software Engineering student, looking for a <strong>professional internship</strong> (the last requirement to graduate). Alongside my coursework, I've spent the last <strong>4 years building self-taught projects</strong>: bots, automation scripts, full-stack systems connected to embedded hardware, and more recently, <strong>local-first AI applications</strong> (audio transcription + RAG running entirely on my own machine, no cloud dependency).

I'm particularly interested in designing robust architectures (Domain-Driven Design, offline-first sync, "Server as the Source of Truth" systems) and software that talks directly to hardware (ESP32, Arduino) or to locally-running AI models.

My main drive is solving everyday problems by building tools with software and hardware.
</p>

---
###

<h2>Educación / Education</h2>

<ul>
  <li><strong>Ingeniería de Software</strong> — Institución Universitaria de Colombia (IUC) - En práctica profesional (último requisito para graduarme) / Currently in professional internship (final graduation requirement)</li>
  <li><strong>Técnico laboral en desarrollo web</strong> — Universidad Autónoma de Bucaramanga (UNAB) — 2023</li>
</ul>

---
###

<h2>Tecnologías / Technologies</h2>

<ul>
  <li><strong>Lenguajes / Languages:</strong> Python, JavaScript, TypeScript, Rust, Dart, C++ (Arduino), C#, AutoHotKey (AHK)</li>
  <li><strong>Frontend:</strong> React 18/19, Astro, Flutter, TailwindCSS, Vite, Wouter, Electron</li>
  <li><strong>Backend:</strong> Node.js + Express, Python (AsyncIO, WebSockets), Rust (Axum), REST APIs</li>
  <li><strong>Bases de Datos / Databases:</strong> MongoDB + Mongoose, MySQL, SQLite, Redis, Qdrant (vector DB)</li>
  <li><strong>IA / Datos:</strong> Whisper (whisper-rs), pipelines RAG (retrieval + reranking + generación), Ollama (LLMs locales), MCP (Model Context Protocol)</li>
  <li><strong>Hardware / IoT:</strong> ESP32, Arduino, sensores (MQ-4 gas, efecto Hall, Potenciómetro, Encoder Rotativo), dispositivos HID, WebSockets para IoT</li>
  <li><strong>Testing:</strong> Pytest, Jest, Playwright</li>
  <li><strong>Herramientas / Tools:</strong> Docker, Git, uv, pnpm, Bun</li>
</ul>

---
###

<h2>Arquitectura y Buenas Prácticas / Architecture & Best Practices</h2>

<ul>
  <li><strong>Arquitectura por capas</strong> (Domain / Infrastructure / Interface) en proyectos Python, inspirada en Clean/Hexagonal Architecture.</li>
  <li><strong>Offline-first & "Server as the Source of Truth":</strong> sistemas cliente-servidor que funcionan sin conexión y sincronizan por timestamps, resolviendo conflictos siempre a favor del servidor.</li>
  <li><strong>Pipelines de IA local (RAG):</strong> chunking, embeddings, retrieval, reranking y generación, sin depender de servicios en la nube ni GPU dedicada.</li>
  <li><strong>MVC</strong> en APIs REST (Node.js/Express) con validación de esquemas (Zod) y esquemas de autenticación basados en tokens (JWT o tokens opacos con revocación vía Redis, según el proyecto).</li>
  <li>Testing automatizado (Pytest, Jest) y documentación técnica extensa en cada repositorio (carpetas <code>docs/</code>, TODOs versionados, decisiones de arquitectura documentadas).</li>
</ul>

---
###

<h2>Proyectos Destacados / Featured Projects</h2>

### 🔹 Transcripción de audio + RAG local-first (Rust)

**[SpeechToTextRust](https://github.com/Sebaxsus/SpeechToTextRust)** (backend) + **[Trasncripts-UI](https://github.com/Sebaxsus/Trasncripts-UI)** (frontend)

Sistema para transcribir grabaciones largas de reuniones (~5h en promedio) usando Whisper corriendo 100% en local (`whisper-rs`), indexar el contenido semánticamente en Qdrant con embeddings de Ollama, y responder preguntas sobre esas transcripciones vía RAG (retrieval + reranking + generación) — sin depender de la nube ni de GPU dedicada. Expone una API REST pensada para integrarse fácilmente desde cualquier tipo de interfaz, y para usuarios no técnicos incluye un cliente web (`Astro` + Astro Islands + `React` + `TypeScript`) que permite subir tanto audio como video (extrayendo solo la pista de audio), monitorear el estado de cada trabajo en tiempo real vía **Polling**, escuchar segmentos puntuales y preguntar sobre el corpus completo. Expone además un servidor MCP de solo lectura.

System that transcribes long meeting recordings (~5h average) using Whisper running fully locally (`whisper-rs`), semantically indexes the content in Qdrant with Ollama embeddings, and answers questions about those transcripts via RAG (retrieval + reranking + generation) — no cloud services, no dedicated GPU required. It exposes a REST API designed to be integrated easily from any kind of interface, and for non-technical users it includes a web client (`Astro` + Astro Islands + `React` + `TypeScript`) that accepts both audio and video uploads (extracting only the audio track), tracks each job's status in real time via **Polling**, lets you listen to specific segments, and lets you query the whole corpus. It also exposes a read-only MCP server.

> *Tecnologías*: Rust, Axum, whisper-rs, Qdrant, Ollama, MCP (rmcp), Astro, React, TypeScript
>
> [Backend](https://github.com/Sebaxsus/SpeechToTextRust) | [Frontend](https://github.com/Sebaxsus/Trasncripts-UI)

---

### 🔹 Ecosistema IoT: sensor de gas ESP32 → servidor → dashboard → app móvil

**[ESP32-PythonWebSocketServer](https://github.com/Sebaxsus/ESP32-PythonWebSocketServer)** + **[PaginaDashboardSensor](https://github.com/Sebaxsus/PaginaDashboardSensor)** + **[proyectoFinal-Moviles](https://github.com/Sebaxsus/proyectoFinal-Moviles)**

Pipeline completo de hardware a interfaz: comienza en un ESP32 WROOM que envía, mediante WebSocket, las lecturas de un sensor de gas MQ-4 (metano) convertidas por su ADC de 12 bits (Analog to Digital Converter), hacia un servidor en Python (arquitectura por capas Domain/Infrastructure/Interface, SQLite, pytest, logger propio) que alimenta un dashboard web en tiempo real construido con Astro + React. Además, como entrega final del curso de Desarrollo Móvil, adapté el mismo caso de uso a un mockup en Flutter (modo oscuro, gráfico de líneas con `CustomPainter`) para monitoreo desde el celular.

Full hardware-to-interface pipeline: it starts with an ESP32 WROOM that streams readings from an MQ-4 gas (methane) sensor — converted through its 12-bit ADC (Analog-to-Digital Converter) — over WebSocket to a Python server (layered Domain/Infrastructure/Interface architecture, SQLite, pytest, custom logger), which feeds a real-time web dashboard built with Astro + React. As the final project for my Mobile Development course, I adapted the same use case into a Flutter mockup (dark mode, custom line chart with `CustomPainter`) for on-the-go monitoring.

> *Tecnologías*: Python (WebSockets, AsyncIO), ESP32/C++, SQLite, Pytest, Astro, React, Flutter/Dart
>
> [Firmware ESP32](https://github.com/Sebaxsus/ESP32-PythonWebSocketServer/tree/main/ESP32/Ejemplo_WIFI_ESP32_Sensor) | [Servidor Python](https://github.com/Sebaxsus/ESP32-PythonWebSocketServer) | [Dashboard Web](https://github.com/Sebaxsus/PaginaDashboardSensor) | [App móvil (Flutter, entrega U)](https://github.com/Sebaxsus/proyectoFinal-Moviles)

---

### 🔹 App de finanzas del hogar, offline-first

**[Mi_Primer_Electron](https://github.com/Sebaxsus/Mi_Primer_Electron)** (desktop) + **[Server-App-Facturas](https://github.com/Sebaxsus/Server-App-Facturas)** (servidor)

Aplicación de escritorio hecha con `Electron JS` (Chromium) para llevar el control de ahorros, arriendo y recibos de servicios públicos del hogar, diseñada bajo el principio **"Server as the Source of Truth"** del mismo modo funciona completamente offline, marca los cambios locales con el estado *pending* y los sincroniza periódicamente con el servidor, resolviendo cualquier conflicto siempre a favor del servidor **SaSOT**. El backend (`Node.js` + `TypeScript` + `Express` + `MongoDB&Mongoose`) valida, deduplica y persiste los datos de forma centralizada para todos los usuarios de la casa.

El frontend, al estar pensado para funcionar tanto en local como en una red de usuarios gestionada por un servidor central, incluye técnicas de seguridad como comparación en tiempo constante (`crypto.timingSafeEqual`) al verificar el hash de las credenciales del usuario (derivado con PBKDF2 + salt), evitando ataques de temporización basados en la diferencia de tiempo que toma comparar el hash.

Desktop application made with `Electron JS` (Chromium) to track household savings, rent, and utility bills, designed around a **"Server as the Source of Truth"** principle: it works fully offline, marks local changes as *pending*, and periodically syncs with the server, always resolving conflicts in the server's favor. The backend (Node.js + TypeScript + Express + MongoDB/Mongoose) validates, deduplicates, and centrally persists data for every user in the household.

The frontend, designed to work both locally and across a network of users managed by a central server, includes security techniques such as constant-time comparison (`crypto.timingSafeEqual`) when verifying the user's credential hash (derived with PBKDF2 + salt), preventing timing attacks based on how long the hash comparison takes.

> *Tecnologías*: Electron, JavaScript/TypeScript, Node.js, Express, MongoDB, Mongoose, JWT
>
> [App de Escritorio](https://github.com/Sebaxsus/Mi_Primer_Electron) | [Servidor](https://github.com/Sebaxsus/Server-App-Facturas)

---

### 🔹 Plataforma Fullstack de Animes y Mangas

**[MiPaginaReact](https://github.com/Sebaxsus/MiPaginaReact)** (frontend) + **[PaginaAnimes-Back](https://github.com/Sebaxsus/PaginaAnimes-Back)** (backend)

Biblioteca web de animes y mangas con frontend en React (TailwindCSS, componentes reutilizables, manejo de sesión con refresh de tokens). Backend API REST en `Express` bajo arquitectura MVC, con middleware estricto de CORS y rate-limiting, validación de esquemas con `Zod`, y un sistema de autenticación propio: tokens opacos (no JWT) generados con el módulo nativo `crypto` de Node y validados contra `Redis` (con expiración e invalidación inmediata de sesión), devueltos en un formato de respuesta compatible con OAuth2 (`access_token`, `refresh_token`, `token_type: Bearer`, `expires_in`) y atados a IP + user-agent como defensa extra contra robo de sesión. Consultas SQL optimizadas en `MySQL` (análisis de planes de ejecución), capa de persistencia con patrón Repository (implementaciones intercambiables en memoria y en MySQL) y pruebas unitarias/de integración con `Jest`.

Anime/manga catalog web app with a React frontend (TailwindCSS, reusable components, session handling with token refresh). REST backend in `Express` following an MVC architecture, with strict CORS and rate-limiting middleware, schema validation with `Zod`, and a custom authentication system: opaque tokens (not JWT) generated with Node's native `crypto` module and validated against `Redis` (with expiration and immediate session revocation), returned in an OAuth2-compatible response shape (`access_token`, `refresh_token`, `token_type: Bearer`, `expires_in`) and bound to IP + user-agent as an extra defense against session theft. Optimized SQL queries in `MySQL` (execution-plan analysis), a Repository-pattern persistence layer (swappable in-memory and MySQL implementations), and unit/integration tests with `Jest`.

> *Tecnologías*: React, TailwindCSS, Node.js, Express, MySQL, Zod, Redis, bcrypt, Jest
>
> [Frontend](https://github.com/Sebaxsus/MiPaginaReact) | [Backend](https://github.com/Sebaxsus/PaginaAnimes-Back)

---

#### 🔹 Otros proyectos / Other projects

- 🎵 **[Bot de Música para Discord](https://github.com/Sebaxsus/dc_bot_py)** — Bot construido con `discord.py`, `spotipy` y `yt-dlp` para reproducir música de YouTube/Spotify, con gestión de colas, autocompletado de comandos y despliegue vía Docker. *(Python, discord.py, AsyncIO, FFmpeg, Docker)*

- 💬 **[Chatbot educativo — entrega final de universidad](https://github.com/Sebaxsus/ChatbotFront)** — Réplica de la interfaz de OpenEnglish con un chatbot integrado, desarrollada en React + Vite como proyecto final de curso. *(React, Vite, Axios, TailwindCSS)*

- 🍅 **[Productivity Timer — Extensión de VSCode](https://github.com/Sebaxsus/Mi_Primera_Extension_VSCode)** — Temporizador Pomodoro con sistema de rachas, puntos, logros y alarmas personalizables (archivo local, YouTube o Spotify). *(TypeScript, VSCode Extension API)*

- ⏭️ **[Skip Ad YouTube](https://github.com/Sebaxsus/Script_Skip_Ad_Chrome)** — Tres enfoques distintos para automatizar el salto de anuncios en YouTube: extensión JS, script AutoHotKey y script en Python con Playwright + Chrome DevTools Protocol. *(JavaScript, AHK, Python, Playwright, CDP)*

- 🚁 **[Simulador de Vuelo — Dispositivo HID con Arduino](https://github.com/Sebaxsus/SimuladorDeVueloArduino)** — Colectivo, cíclico y pedales físicos construidos con Arduino, sensores de efecto Hall, potenciómetros y encoders, expuestos al sistema operativo como dispositivo HID. *(C++, Arduino, Electrónica)*

#### 🔹 Más información en mi portafolio

Ver en: 🌐 [Portafolio](https://portafolio-astro-phi.vercel.app/)

---
###

<h2>🌐 Contribuciones Open Source</h2>

<ul>
  <li>
    Contribuciones directas a <a href="https://github.com/Davele12/mcp-git-assistant" target="_blank" referrerpolicy="no-referrer">mcp-git-assistant</a>
  </li>
  <li>
    Soporte comunitario y debugging en <a href="https://github.com/AsyncFuncAI/deepwiki-open" target="_blank" referrerpolicy="no-referrer">deepwiki-open</a> a través de su comunidad en Discord
  </li>
</ul>

---

###

<h2>📄 Documentación / Documentation</h2>

<h3>ESPAÑOL 🇪🇸</h3>
<p>
  Todos mis proyectos están acompañados por documentación técnica y guías de usuario para facilitar su comprensión, implementación y mantenimiento.
</p>

---

<h3>ENGLISH 🇺🇸</h3>
<p>
  All my projects include technical documentation and user manuals for easier understanding, deployment, and maintenance.
</p>

---
###

<h2>🧭 En constante aprendizaje / Always learning</h2>

<p>
  Me mantengo en constante mejora, aprendiendo nuevas arquitecturas, herramientas y metodologías para seguir construyendo software que impacte en el mundo real.
</p>
<p>
  I'm constantly improving, learning new architectures, tools, and methodologies to continue building software that impacts the real world.
</p>

<hr/>

###


<img align="right" height="150" src="https://cdn.7tv.app/emote/01GEEHRQYG0006MCY6R6BPV3HB/4x.avif"  />

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="30" alt="typescript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-original.svg" height="30" alt="rust logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="30" alt="react logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/astro/astro-original.svg" height="30" alt="astro logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="30" alt="csharp logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg" height="30" alt="dart logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg" height="30" alt="flutter logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="30" alt="nodejs logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" height="30" alt="mongodb logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="30" alt="mysql logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" height="30" alt="redis logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" height="30" alt="docker logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/arduino/arduino-original.svg" height="30" alt="arduino logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/discordjs/discordjs-original.svg" height="30" alt="discordjs logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="30" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="30" alt="github logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jest/jest-plain.svg" height="30" alt="jest logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" height="30" alt="linux logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="30" alt="vscode logo"  />
</div>

###

<div align="left">
  <a href="https://www.linkedin.com/in/TU-USUARIO-DE-LINKEDIN" target="_blank" referrerpolicy="no-referrer">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />
  </a>
  <a href="mailto:tu-correo@ejemplo.com">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="gmail logo"  />
  </a>
  <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="discord logo"  />
</div>

###

<br clear="both">

###
<div style="align-items: center;display: flex;flex-direction: row;gap: 4px;">
  <img src="https://raw.githubusercontent.com/Sebaxsus/Sebaxsus/output/snake.svg" alt="Snake animation" width="600"/>
  <img align="right" height="130" src="https://cdn.7tv.app/emote/01G044NFSG00033Y3V2VD0Z8KK/4x.avif"  />
</div>

###

<br clear="both">

###
