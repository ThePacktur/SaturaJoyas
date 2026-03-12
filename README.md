# SaturaJoyas
Quest HTML

Sitio web estático de **Saturina Joyas** enfocado en catálogo, presencia de marca y contacto.

## Estructura (separación por capas)

```text
SaturaJoyas/
├── README.md
└── Quest HTML2/
    ├── index.html          # Estructura y contenido (HTML)
    ├── css/
    │   ├── reset.css       # Reset base
    │   └── styles.css      # Estilos del proyecto
    ├── js/
    │   └── main.js         # Comportamiento cliente (validaciones / utilidades)
    ├── http/
    │   └── security-headers.conf  # Propuesta de cabeceras HTTP de seguridad
    └── img/
```

## Mejoras aplicadas

- **Separación CSS, JS y HTTP**:
  - `index.html` solo maneja estructura y contenido HTML (sin estilos ni scripts embebidos).
  - `css/styles.css` centraliza estilos.
  - `js/main.js` encapsula validación de formularios y utilidades de UI.
  - `http/security-headers.conf` documenta políticas de seguridad para servidor.
- **Accesibilidad y calidad**:
  - Etiquetas semánticas, navegación clara, formularios con labels y validación.
- **Seguridad frontend/server-ready**:
  - Enlaces externos protegidos (`noopener noreferrer`).
  - Embebido de video con `youtube-nocookie`.
  - Cabeceras HTTP recomendadas para producción.

## Ejecución local

```bash
python3 -m http.server 8000 --directory "Quest HTML2"
```

Abrir en navegador:

- `http://localhost:8000`

## Recomendaciones para producción

- Configurar las cabeceras de `Quest HTML2/http/security-headers.conf` en el servidor real.
- Activar HTTPS y redirección forzada HTTP->HTTPS.
- Incorporar CI con lint de HTML/CSS/JS y auditoría Lighthouse.