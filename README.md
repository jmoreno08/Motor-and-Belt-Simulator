# Surfer’s Series One — Simulador universal de motorreductores y banda

Aplicación web estática para visualizar una banda continua con cerdas accionada por un motorreductor DC. Incluye modo Cliente e Ingeniería, selector Español / English, indicadores de giro, campos con ayudas y exportación de candidatos.

## Inicio rápido

1. Abre `index.html` en un navegador moderno.
2. Alternativamente, desde la carpeta del proyecto ejecuta `python -m http.server 8000` y visita `http://localhost:8000`.
3. Introduce las especificaciones del **eje de salida** del motorreductor (RPM sin carga y nominales), el voltaje y el diámetro efectivo del rodillo motriz.
4. Ajusta el voltaje y observa la velocidad de banda. Usa modo Ingeniería para parámetros de carga y estimaciones adicionales.

No requiere compilación, paquetes externos, servidor de aplicación ni acceso a internet.

## Estructura

```text
surfers_motor_sim/
├── index.html                 # Interfaz principal
├── assets/
│   ├── css/styles.css         # Estilos y diseño adaptable
│   └── js/
│       ├── simulator.js       # Cálculos, animación, controles y exportación
│       └── i18n.js            # Traducciones y cambio de idioma ES/EN
├── docs/
│   └── MODELO.md              # Alcance técnico y supuestos
└── README.md
```

## Notas

- Los valores de velocidad y corriente son estimaciones, no resultados de ensayos.
- La animación sigue el cálculo cinemático; en pantallas puede aparecer aliasing/efecto estroboscópico a altas RPM.
- No es un simulador de seguridad capilar, ni verifica atrapamientos, temperatura, autonomía o vida útil.
- Los datos y preferencias guardados usan el almacenamiento local del navegador, cuando está disponible.
- El orden de los scripts importa: `simulator.js` debe cargarse antes que `i18n.js`.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub y sube **el contenido** de esta carpeta a la raíz de la rama `main` (no la carpeta contenedora).
2. En el repositorio abre **Settings → Pages → Build and deployment**.
3. Selecciona **Source: GitHub Actions**.
4. En **Actions**, ejecuta `Deploy GitHub Pages` si no se inició automáticamente.
5. Espera a que el workflow termine correctamente. La dirección será `https://USUARIO.github.io/REPOSITORIO/` (o `https://USUARIO.github.io/` si el repositorio se llama `USUARIO.github.io`).

El sitio es estático; no requiere Node.js ni servidor backend. Las rutas de recursos son relativas para funcionar bajo el subdirectorio de GitHub Pages.
