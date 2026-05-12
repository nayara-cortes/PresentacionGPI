# ContentFlow — Sistema de Diseño

**ContentFlow** es una aplicación web de gestión económica, fiscal y administrativa orientada a **autónomos creadores de contenido digital** (streamers, YouTubers, influencers, podcasters, creadores de cursos, etc.). El sistema centraliza clientes, proveedores, presupuestos, facturación (cumple normativa **VERIFACTU**), cobros/pagos, libros contables, IVA, retenciones IRPF y un panel analítico con KPIs específicos del sector creator.

> Este sistema de diseño existe para presentar el proyecto académico de ContentFlow — **Gestión de Proyectos Informáticos, curso 2025-26, Grupo J11-4**. Su uso principal son las **diapositivas de la presentación final** y mockups de producto que aparecen dentro de esas slides.

---

## Contexto de origen

- **Asignatura:** Gestión de Proyectos Informáticos (GPI), curso 2025-26
- **Universidad:** Universidad de Alicante — I²ADE (Doble Grado Ingeniería Informática + ADE)
- **Profesor:** Carlos José Villagrá Arnedo
- **Grupo:** J11-4
- **Versión documento:** 2
- **Equipo (6):** Nayara Paloma Cortés Quesada · Santiago Redondo De La Rica · Enrique Cuesta Quintana · Adrián José Guerra Castro · Christian Campello Cornejo · Francisco Navarro Martínez
- **Deadline académico:** 14 de mayo de 2026

### Fuentes consumidas
- `uploads/planning.docx.pdf` — Documento de Planificación v2 completo (60 páginas). Texto completo extraído en `source/planning_full.txt`.
- Sin codebase ni Figma asociados — el sistema visual de marca **se ha definido aquí desde cero** para servir a la presentación. Si en el futuro existe un proyecto de código real, debería iterarse este sistema contra él.

### Estructura de la presentación (4 bloques)
1. **Introducción** — objetivos generales + requerimientos funcionales y no funcionales + restricciones (personal, tiempo, presupuesto, legales, técnicas, tecnológicas).
2. **Estimación de costes** — Componentes de Coste, Ley de Parkinson, Pricing to Win, Puntos Objeto (COCOMO 2), Juicio Experto + comparativa.
3. **Análisis de riesgos** — identificación, prioridades, planes de contingencia, mecanismos de seguimiento.
4. **Planificación** — plantilla, plan general, plan detallado *(capturas pendientes de añadir por el equipo)*.

---

## Índice del repositorio

```
/
├── README.md                  ← este documento
├── SKILL.md                   ← skill cross-compatible con Agent Skills
├── colors_and_type.css        ← tokens de color + tipo (CSS vars) + estilos semánticos (h1, h2, p, code…)
├── source/
│   └── planning_full.txt      ← texto extraído del PDF original (referencia para slides)
├── assets/
│   ├── logo-mark.svg          ← isotipo (símbolo solo)
│   ├── logo-lockup.svg        ← logotipo completo (mark + wordmark)
│   ├── logo-mono.svg          ← versión monocromática
│   └── pattern-flow.svg       ← textura/patrón de marca
├── preview/                   ← cards del Design System (700×N px)
├── slides/
│   ├── index.html             ← deck demo con todos los layouts
│   └── *.jsx                  ← componentes React de cada layout
└── ui_kit/
    └── index.html             ← mock interactivo del producto ContentFlow (dashboard)
```

---

## CONTENT FUNDAMENTALS — cómo se escribe

**Idioma:** Español de España, registro académico-profesional. Uso de **«vosotros»** para el equipo y **«usted/el usuario»** para el creador final cuando se habla del producto. En slides se prefiere **«nosotros»** colectivo del equipo presentador.

**Tono:**
- **Riguroso, técnico, con seguridad.** Nunca informal, nunca con emoji.
- **Frases declarativas, no comerciales.** Evitar adjetivos vacíos («increíble», «mejor de su clase»).
- **Datos concretos antes que afirmaciones.** Siempre que haya un número, va antes que la prosa.
- **Impersonal de tercera persona** en documentación («el sistema deberá…», «la aplicación se desplegará…»).
- **Activa y directa** en titulares de slide («Estimamos 25 personas-mes», no «Se ha estimado…»).

**Casing:**
- Títulos de slide: **Capitalización tipo frase** («Estimación de costes», no «Estimación De Costes»).
- Identificadores funcionales en **MAYÚSCULAS_GUION_BAJO** (heredado del PDF: `FACT_E_REG`, `IVA_RESUMEN`).
- Bloques de sección: numeración decimal (`1.`, `1.1.`, `1.1.2.`).
- Acrónimos siempre en mayúsculas: VERIFACTU, IVA, IRPF, RGPD, LSSI-CE, CRUD, KPI, MVP, COCOMO 2, PROD, PO, NOP.

**Iconografía textual:** **Sin emoji nunca.** Para listas se usan viñetas tipográficas: `●` (nivel 1), `–` (nivel 2). Para énfasis: **negrita** sobre cursiva.

**Ejemplos canónicos del documento original (a imitar):**
- *«El objetivo principal es diseñar y desarrollar una aplicación web orientada a autónomos del sector de creadores de contenido…»*
- *«Por tanto, el esfuerzo total estimado para la realización del proyecto es de 1.920 horas.»*
- *«El resultado de 25 personas-mes equivale, para un equipo de 6 personas trabajando a jornada completa, a una duración estimada de aproximadamente 4.17 meses.»*
- *«No obstante, consideramos prudente tener en cuenta la estimación por Puntos de Objeto como señal de alerta…»*

**Vibe global:** Memoria técnica universitaria + producto SaaS moderno. Ni plantilla corporate genérica, ni pitch de startup hype.

---

## VISUAL FOUNDATIONS — la materia

**Palette filosofía.** Cálido + serio. ContentFlow vive en la intersección de dos mundos: el de los **creadores** (cálido, expresivo, vital) y el **fintech/contable** (sobrio, fiable, exacto). La paleta resuelve esa tensión con un coral cálido contra un ink profundo, sobre fondos crema para evitar el azul-blanco SaaS por defecto.

| Rol | Token | Hex | Uso |
|---|---|---|---|
| Primario / acento | `--coral` | `#F25C3F` | CTA, highlights, marca |
| Ink / texto principal | `--ink` | `#0F1729` | Headings, body, charts |
| Cream / fondo principal | `--cream` | `#FAF6F0` | Background slides, surface base |
| Lima / éxito-financiero | `--lime` | `#A8D86F` | KPI positivos, ingresos, deltas + |
| Ámbar / advertencia | `--amber` | `#F2B33F` | Riesgos medios, vencimientos |
| Rojo / riesgo | `--alert` | `#D43F3A` | Riesgos críticos, gastos, deltas − |
| Slate / texto secundario | `--slate` | `#5A6478` | Labels, captions, footnotes |

**Tipografía.** Tres familias, tres roles muy delimitados:
- **Bricolage Grotesque** — display, titulares, números grandes. Variable, con un toque editorial-grotesque que rompe con el sans genérico.
- **DM Sans** — body, párrafos, UI, etiquetas. Humanista, legible a 14-18 px.
- **JetBrains Mono** — código, identificadores funcionales (`FACT_E_REG`), valores numéricos en tablas financieras donde se requiere alineación.

> **Sustitución señalada:** No se ha proporcionado paquete de fuentes corporativo. Se sirven desde **Google Fonts** (Bricolage Grotesque, DM Sans, JetBrains Mono). Si el equipo dispone de licencias propias (p.ej. *General Sans*, *Söhne*), reemplazar en `colors_and_type.css`.

**Spacing / grid.** Escala basada en `4px` (`--s-1` a `--s-16`). Todas las slides son **1920×1080** con un padding lateral fijo de `120px` (`--slide-pad-x`) y vertical de `100px` (`--slide-pad-y`).

**Backgrounds.** Tres tratamientos:
1. **Crema plano (`--cream`)** — slides de contenido, tablas, listados. Por defecto.
2. **Ink profundo (`--ink`)** — slides divisoras de sección y la portada. Inversa, alto impacto.
3. **Coral saturado (`--coral`)** — slides de cita o dato hero. Uso muy limitado (1-2 por deck).

No hay gradientes. No hay full-bleed photography. El brand vive en color plano + tipografía + un patrón geométrico de líneas finas (`pattern-flow.svg`) usado **muy ocasionalmente** como marca de agua en esquinas.

**Animation.** **Cero animación dentro de las slides.** Las transiciones entre slides son las que aporta el navegador del usuario o un `fade` de 200ms en deck-stage. La presentación es académica y debe leerse como un documento, no como un pitch de startup.

**Hover / press.** Los componentes interactivos del UI kit usan:
- Hover: opacity `0.85` o background un step más oscuro (mezcla 8 % con `--ink`).
- Press: `transform: translateY(1px)` + sombra reducida.
- Focus: outline coral 2px con offset 2px.

**Borders & shadows.** Sistema sobrio:
- Bordes: `1px solid color-mix(in srgb, var(--ink) 10%, transparent)`. Nunca borders coloreados accent salvo en estado de error.
- Sombras: 3 niveles — `--shadow-sm` (cards de KPI), `--shadow-md` (modales), `--shadow-lg` (focus / popover). Sin glow ni neumorfismo.

**Radii.** `--r-sm: 6px` (chips, inputs) · `--r-md: 12px` (cards) · `--r-lg: 20px` (paneles grandes, hero KPI) · `--r-pill: 999px` (badges).

**Transparency / blur.** No usar `backdrop-filter`. La única transparencia permitida son las mezclas con `color-mix()` para variantes de los tokens base (e.g. `--ink-90`, `--coral-15`).

**Imagery vibe.** Cuando se inserten capturas reales (de la app, de Gantt, etc.) se aplica un marco con `border-radius: 12px` + `box-shadow: var(--shadow-md)` + `border: 1px solid color-mix(in srgb, var(--ink) 8%, transparent)`. **Sin tratamientos B&N, grain o duotone** — las capturas se muestran tal cual, los datos del proyecto son el contenido.

**Layout rules (slides).**
- Header de slide siempre en la posición `(--slide-pad-x, --slide-pad-y)`.
- Numerador `01 / 24` y sección activa siempre en la esquina superior derecha.
- Logo en la esquina inferior izquierda en blanco coral (excepto portada y dividers).
- Pie con `J11-4 · GPI 2025-26` siempre visible salvo en portada.

---

## ICONOGRAPHY

**Sistema:** **Lucide Icons** vía CDN (`https://unpkg.com/lucide@latest`). Stroke `1.75px`, esquinas redondeadas, estilo línea — encaja con el carácter sobrio del sistema sin caer en el barroco.

> **Sustitución señalada:** Sin codebase, no había icon set propio. Lucide es la elección por consistencia visual + cobertura. Si más adelante el equipo elige otro set (Phosphor, Tabler), reemplazar el CDN y reescalar el stroke.

**Reglas de uso:**
- Los iconos en slides son **decorativos discretos**, no protagonistas. Tamaño base `20px`, color `--slate` salvo cuando representan el dato hero (entonces `--coral`).
- En el dashboard del UI kit los iconos son `18px` en menús, `16px` en estados, `24px` en headers de tarjeta KPI.
- **Sin emoji** en ningún contexto del sistema. Sin caracteres unicode usados como icono (★, ✓, etc.) — usar Lucide `Star`, `Check`, etc.

**Logo:** El isotipo de ContentFlow es una **«C» geométrica abierta** que evoca un flujo (espiral de dos trazos coral). El logotipo se compone con la palabra «ContentFlow» en Bricolage Grotesque ExtraBold. Tres variantes en `assets/`: lockup horizontal, mark solo, monocromo ink.

---

## SKILL invocation

Si descargas este sistema como Agent Skill: ver `SKILL.md`. La idea es invocarlo cuando vayas a generar más slides para la presentación, mockups del producto o material académico relacionado con ContentFlow.

---

## CAVEATS conocidos

- **Sin codebase ni Figma reales** — el visual identity es propuesta a iterar.
- **Fonts** servidas desde Google Fonts; si hay licencias propias, sustituir.
- **Iconos** desde Lucide CDN — no se han copiado SVGs locales.
- **Slides 4 (Planificación)** quedan con placeholders donde el equipo pegará capturas de la plantilla, plan general y plan detallado (Gantt).
