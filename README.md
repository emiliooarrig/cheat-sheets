# Cheat Sheets

Sitio web estático que reúne una colección de **hojas de trampa** (cheat sheets) con códigos y configuraciones utilizados en proyectos personales y académicos. Funciona como un repositorio de consulta rápida para problemas comunes en el desarrollo de software.

## ✨ Características

- Página principal con un menú de todas las hojas disponibles.
- Cada hoja de trampa cuenta con bloques estilo terminal de Linux para mostrar comandos y comentarios.
- Tema oscuro moderno con detalles de degradado (glassmorphism sutil).
- Diseño responsivo (escritorio y móvil).
- Navegación consistente: navbar con regreso al menú y footer con enlaces básicos.
- Sección de contacto (LinkedIn, GitHub y Proton Mail).

## 📁 Estructura del proyecto

```
cheat_codes/
├── index.html              # Página principal con el menú de hojas y contacto
├── style.css               # Estilos de la página principal
├── img/
│   └── pixelart.png        # Imagen del creador
├── cheatsheets/
│   ├── generals.css        # Estilos compartidos por todas las hojas
│   ├── vnc/
│   │   └── vnc.html        # Hoja: configuración de servidor VNC en Linux
│   └── n8n/
│       └── n8n.html        # Hoja: instalación de n8n con Docker (Podman)
├── mds_cheatsheets/        # Fuentes en Markdown (ignorado por git)
└── README.md
```

## 📑 Hojas disponibles

| Hoja | Descripción |
|------|-------------|
| **VNC** | Instalación y configuración de un servidor VNC (TigerVNC) en Linux (RHEL). |
| **n8n** | Instalación de n8n (self-hosted) con contenedores en Docker (Podman). |

## 🚀 Uso

Al ser un sitio estático no requiere dependencias ni proceso de compilación. Basta con abrir `index.html` en el navegador:

```bash
# Abrir directamente
xdg-open index.html      # Linux

# O servirlo con un servidor local (recomendado)
python3 -m http.server 8000
# Luego visita http://localhost:8000
```

## 🛠️ Agregar una nueva hoja de trampa

1. Crea una carpeta dentro de `cheatsheets/` (por ejemplo `cheatsheets/mi-tema/`).
2. Crea el archivo HTML siguiendo la estructura de `cheatsheets/vnc/vnc.html` (navbar, header, main y footer).
3. Enlaza la hoja de estilos compartida: `<link rel="stylesheet" href="../generals.css">`.
4. Agrega la ruta de la nueva hoja a la lista `.list-sheets` en `index.html`.
5. Añade el enlace a la navegación del footer en las demás hojas si corresponde.

## 🎨 Tecnologías

- HTML5
- CSS3 (variables, flexbox, grid)
- Fuente [Quicksand](https://fonts.google.com/specimen/Quicksand) vía Google Fonts

---

Creado con ❤ en México por **Emilio Guzmán**
