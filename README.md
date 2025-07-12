<h2 align="left">Hi 👋! My name is Juan Sebastian Garcia and I'm a Software Engineer Student from Colombia</h2>

###

<h2>🧑‍💻 Sobre mí / About Me</h2>

<h3>ESPAÑOL 🇪🇸</h3>
<p>
Estudiante de Ingeniería de Software (9.º semestre), con un enfoque práctico en el desarrollo de soluciones reales que integran software, hardware, redes y automatización. Me especializo en tecnologías modernas como Python, React, WebSockets y Arduino, desarrollando sistemas escalables, en tiempo real y con documentación técnica completa.

He trabajado en proyectos Full Stack, IoT, automatización de tareas del sistema y bots para Discord, con una fuerte orientación a la arquitectura de software (MVC, Domain-Driven Design) y un interés genuino en redes, electrónica y telecomunicaciones.
</p>
<hr/>
<h3>ENGLISH 🇺🇸</h3>
<p>
  I'm a Software Engineering student (9th semester), focused on building real-world solutions that integrate software, hardware, networking, and automation. I specialize in modern technologies such as Python, React, WebSockets, and Arduino, developing scalable, real-time systems with complete technical documentation.

I've worked on Full Stack applications, IoT integrations, system automation, and Discord bots, with a strong focus on software architecture (MVC, Domain-Driven Design) and a genuine interest in networking, electronics, and telecommunications.
</p>

---
###

<h2>🛠️ Tecnologías / Technologies</h2>

<ul>
  <li><strong>Lenguajes / Languages:</strong> C++, Python, Java, JavaScript, C#, AHK</li>
  <li><strong>Frontend:</strong> React, Astro, TailwindCSS, SVG personalizados, Micro-Frontend</li>
  <li><strong>Backend:</strong> Python (REST, WebSockets), Node.js + Express, MySQL, SQLite3</li>
  <li><strong>Testing y Automatización:</strong> Pytest, pytest-asyncio, Playwright, Logger, Jest</li>
  <li><strong>Sistemas y Redes:</strong> Linux, Wireshark, WebSocket Servers, ESP32</li>
  <li><strong>Microcontroladores y Electrónica:</strong> Arduino, HID Devices, Potenciómetros, Sensores Hall</li>
  <li><strong>Otros:</strong> FFmpeg, Discord.py, yt-dlp, Subprocesos Python, Documentación técnica + de usuario</li>
</ul>

---
###

<h2>🧠 Arquitectura y Buenas Prácticas / Architecture & Best Practices</h2>

<ul>
  <li>Uso de <strong>MVC</strong> para separación de lógica y escalabilidad.</li>
  <li>Refactorización de proyectos hacia <strong>Domain-Driven Design (DDD)</strong>.</li>
  <li>Uso de <strong>HTTP status codes</strong> correctos en desarrollo de APIs REST.</li>
  <li>Separación de responsabilidades y técnicas para evitar el <strong>Global Interpreter Lock (GIL)</strong> en Python usando <strong>asincronía y subprocesos</strong>.</li>
</ul>

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

<h2>🚀 Proyectos Destacados / Featured Projects</h2>

#### 🔹 **Dashboard IoT en Tiempo Real con ESP32 + WebSockets + Astro/React**

Servidor en Python con WebSockets que comunica sensores ESP32. Guarda eventos en tiempo real y usa un webhook para identificar clientes conectados y actualizar un dashboard web hecho con Astro + React. Incluye pruebas automatizadas (pytest), logger personalizado y base de datos con SQLite3.

Python server with WebSockets that communicates with ESP32 sensors. It records events in real time and uses a webhook to identify connected clients and update a web dashboard built with Astro + React. It includes automated tests (pytest), a custom logger, and a SQLite3 database.

> *Tecnologías*: Python, WebSockets, Astro, React, Pytest, AsyncIO, SQLite3
>
>  [Sensor](https://github.com/Sebaxsus/ESP32-PythonWebSocketServer/blob/main/ESP32/Ejemplo_WIFI_ESP32_Sensor/Ejemplo_WIFI_ESP32_Sensor.ino) | [Backend](https://github.com/Sebaxsus/ESP32-PythonWebSocketServer) | [Frontend](https://github.com/Sebaxsus/PaginaDashboardSensor)

---

#### 🔹 **[Página de Animes Fullstack](https://github.com/Sebaxsus/MiPaginaReact)**

Frontend en React con TailwindCSS y SVGs personalizados. Backend en Express.js (JavaScript-Node.js) con API REST y Paginación, consultas SQL optimizadas usando MySQL Workbench (análisis de tipos de scan) para reducir los tiempos de respuesta y mejorar la experiencia del usuario.

React frontend with TailwindCSS and custom SVGs. Express.js (JavaScript-Node.js) backend with REST API and pagination, optimized SQL queries using MySQL Workbench (scan type analysis) to reduce response times and improve user experience.

> *[Frontend](https://github.com/Sebaxsus/MiPaginaReact)* | *[Backend](https://github.com/Sebaxsus/PaginaAnimes-Back)*

---

#### 🔹 **[Script para Saltar Anuncios de YouTube](https://github.com/Sebaxsus/Script_Skip_Ad_Chrome)**

Solución multiplataforma para omitir anuncios en YouTube / Cross-platform solution to skip ads on YouTube:

- Extensión en JS (limitada por políticas de YouTube) / JS Extension (Limited by YouTube policies)

- Script AHK (funcional en Windows) / AHK Script (Working on Windows)

- Script Python + Playwright usando Chrome DevTools Protocol / Python Script + Playwright using Chrome DevTools Protocol

> *Tecnologías*: JavaScript, AHK, Python, CRDP, Playwright

---

#### 🔹 **Bot de Música para Discord (en producción) | *Repositorio Privado***

Bot funcional con promedio de 8 usuarios diarios. Construido en Python usando `discord.py`, `yt-dlp`, `asyncio` y `FFmpeg`. Maneja recursos asincrónicamente y evita bloqueos por GIL usando subprocesos.

Working bot with an Average of 8 daily users. Develop in Python using `discord.py`, `yt-dlp`, `asyncio` and `FFmpeg`.
Manage resources asynchronously and avoid GIL locks using threads.

> *Tecnologías*: Python, Discord.py, yt-dlp, FFmpeg

---

#### 🔹 **Dispositivo HID para Simulación de Vuelo en Helicóptero | *Repositorio Privado***

Sistema de control físico (colectivo, cíclico, pedales) para simulación precisa de helicópteros. Construido con Arduino, sensores efecto Hall, potenciómetros y encoders.

Physical control system (collective, cyclic, pedals) for precise helicopter simulation. Built with Arduino, Hall effect sensors, potentiometers, and encoders.

> *Tecnologías*: Arduino, HID, Electrónica, Diseño de hardware

---

#### 🔹 **Proyectos con Arduino**

- Reloj digital con display de 7 segmentos / Digital clock with 7-segment display

- Red de sensores con ESP32 y análisis de tráfico vía Wireshark / Sensor network with ESP32 and traffic analysis via Wireshark

---

#### 🔹 Mas información en mi portafolio

Ver en: 🌐 [Portafolio](https://portafolio-astro-phi.vercel.app/)

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

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Sebaxsus&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=Sebaxsus&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>

<img align="right" height="150" src="https://cdn.7tv.app/emote/01GEEHRQYG0006MCY6R6BPV3HB/4x.avif"  />

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="30" alt="react logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="30" alt="csharp logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/anaconda/anaconda-original.svg" height="30" alt="anaconda logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/arduino/arduino-original.svg" height="30" alt="arduino logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/discordjs/discordjs-original.svg" height="30" alt="discordjs logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="30" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="30" alt="github logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="30" alt="java logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jest/jest-plain.svg" height="30" alt="jest logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" height="30" alt="linux logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/markdown/markdown-original.svg" height="30" alt="markdown logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="30" alt="nodejs logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/oracle/oracle-original.svg" height="30" alt="oracle logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/putty/putty-original.svg" height="30" alt="putty logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="30" alt="vscode logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/visualstudio/visualstudio-plain.svg" height="30" alt="visualstudio logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="30" alt="mysql logo"  />
</div>

###

<div align="left">
  <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="discord logo"  />
  <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="gmail logo"  />
  <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />
</div>


###

<br clear="both">

###
<div>
  <img src="https://raw.githubusercontent.com/Sebaxsus/Sebaxsus/output/snake.svg" alt="Snake animation" width="600"/>
  <img align="right" height="130" src="https://cdn.7tv.app/emote/01G044NFSG00033Y3V2VD0Z8KK/4x.avif"  />
</div>

###

<br clear="both">

###
