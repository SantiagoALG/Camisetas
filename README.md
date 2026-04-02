# ⚽ FIFA 2026 — Kit Bracket

Herramienta personal para elegir la mejor camiseta del Mundial FIFA 2026.
Sin dependencias. Abre directo en el navegador.

---

## Estructura

```
fifa-kit-bracket/
├── index.html          ← App completa
├── style.css           ← Estilos
├── data/
│   └── teams.json      ← 48 selecciones en 12 grupos
└── images/
    ├── argentina/
    │   ├── local.png
    │   └── visitante.png
    └── ... (un folder por selección)
```

---

## Cómo usar

### 1. Agregar imágenes

Coloca las imágenes en `images/{id}/local.png` y `images/{id}/visitante.png`.
Los IDs están en `data/teams.json`. También puedes subirlas directo desde la app.

### 2. Abrir la app

Necesitas un servidor local (los navegadores bloquean fetch desde file://).

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```

Luego abre http://localhost:8080

### 3. Flujo

| Paso | Vista | Acción |
|------|-------|--------|
| 01 | Camisetas | Elige local o visitante por país |
| 02 | Grupos | Arrastra para ordenar 1°–4° en cada grupo |
| 03 | Mejores Terceros | Elige 8 de 12 terceros que clasifican |
| 04 | Bracket | Haz clic en el ganador de cada duelo |

---

## Grupos (FIFA 2026)

| Grupo | Selecciones |
|-------|-------------|
| A | Estados Unidos, Canadá, México, Ghana |
| B | Argentina, Ecuador, Chile, Nigeria |
| C | Brasil, Colombia, Venezuela, Senegal |
| D | Francia, Alemania, Bélgica, Marruecos |
| E | España, Portugal, Croacia, Corea del Sur |
| F | Inglaterra, Países Bajos, Austria, Australia |
| G | Italia, Suiza, Dinamarca, Camerún |
| H | Japón, Irán, Uzbekistán, Egipto |
| I | Uruguay, Perú, Bolivia, Sudáfrica |
| J | Turquía, Hungría, Escocia, Nueva Zelanda |
| K | Arabia Saudita, Qatar, Argelia, Mali |
| L | Serbia, Rumanía, Ucrania, Indonesia |

> Los grupos son aproximados. Edita `data/teams.json` para ajustar al sorteo oficial.

---

## GitHub

```bash
git init
git add .
git commit -m "init: fifa kit bracket"
git remote add origin https://github.com/tu-usuario/fifa-kit-bracket.git
git push -u origin main
```

GitHub Pages: Settings → Pages → Source: main → `/root`
