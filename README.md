# ✈️ Plan de Vuelo 247

**CRM y Protocolo FORDEC para Aulas STEAM** · Conferencia SEEC 2027

Web App móvil con interfaz estilo iOS (Apple HIG) que simula una cabina de mando pedagógica: simulador de crisis FORDEC, kit CRM bilingüe y evaluador de proyectos STEAM con Órbitas Pedagógicas.

Presenta: **C.P.A.C. Erick Arturo Sánchez Reus**

## Módulos

- **Inicio:** widgets estilo iOS, telemetría y selector Español / English.
- **Simulador FORDEC:** Facts → Options → Risks → Decision → Execution & Check, con generador de escenarios por IA y Flight Safety Score con comentario del Copiloto IA.
- **Recursos CRM:** checklists de tripulación y señas tácticas en iOS Sheet.
- **Evaluador STEAM con IA:** Órbitas Baja / Media / Alta generadas por IA (con respaldo local si la IA no está disponible), más un chat "Copiloto IA" para preguntas sobre CRM/FORDEC.
- **Comparar resultados:** historial local (en el propio dispositivo) de simulaciones FORDEC y evaluaciones STEAM, con comparación lado a lado.
- **Exportar a GitHub:** botón en la cabecera con descarga de un solo toque (.zip con ambos archivos, o por separado).

## Estructura

```
.
├── index.html   # App completa (HTML + CSS + JS)
└── README.md
```

## Ejecutar en local

```bash
# opción 1: abrir index.html en el navegador
# opción 2: servidor local
python3 -m http.server 8080
```

## Publicar en GitHub

```bash
git init
git add index.html README.md
git commit -m "Plan de Vuelo 247 - SEEC 2027"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/plan-de-vuelo-247.git
git push -u origin main
```

## Desplegar en GitHub Pages

1. Repositorio → **Settings → Pages**.
2. En *Build and deployment* elige **Deploy from a branch**.
3. Selecciona rama **main** y carpeta **/ (root)** → **Save**.
4. Tu app quedará en `https://TU_USUARIO.github.io/plan-de-vuelo-247/`.

## Desplegar en Vercel

1. Entra a vercel.com → **Add New… → Project** e importa el repositorio.
2. Framework Preset: **Other** (sitio estático, sin build).
3. Pulsa **Deploy**.

## Notas

- Las funciones de IA (generador de escenarios, comentario del Copiloto, Evaluador STEAM y chat Copiloto) usan IA real solo dentro de Claude; fuera de Claude (GitHub Pages, Vercel, local) esas funciones muestran un aviso y el Evaluador STEAM usa una heurística local de respaldo.
- El botón "Descargar todo (.zip)" carga JSZip desde cdnjs.cloudflare.com; sin internet, usa los botones de descarga individual.
- El historial de "Comparar resultados" se guarda en el navegador de cada persona (localStorage); no se comparte entre dispositivos.
- Diseñada para verse como iPhone en escritorio y a pantalla completa en móvil.

---

*Maker STEAM Horizonte Cero · SEEC 2027*
