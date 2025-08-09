---
name: Generar Web App Zero-Deps
alwaysApply: false
---

## USER PROMPT — Encargo de Web App basada en los adjuntos

**Contexto:** Te adjunto `git_hub_copilot_and_continue_integration.md` y `GitHub Copilot and Continue Integration.pdf`. Úsalos como **fuente de verdad** para flujo de trabajo y manejo de contexto del repositorio.

**Objetivo:** Crea una **Web App** que cumpla nuestra filosofía **“Zero Dependencies, Maximum Performance”** y los siguientes **pilares**:
- HTML5 puro (semántico)  
- Performance-First (≥95/100 PSI; optimiza LCP/INP/CLS)  
- Client-Side AI prioritaria (Transformers.js / ONNX Web; Web Workers)  
- SEO orgánico  
- Security by Design (OWASP ASVS + GDPR/EU AI Act según riesgo)  
- Progressive Enhancement  
- WCAG 2.1 AA

**Stack específico:**  
Tailwind v4+ **via npx** (no CDN), JS ES6+ vanilla modular, Service Worker + Web Manifest; opcionalmente IA en cliente (Transformers.js, ONNX Runtime Web, MediaPipe, Compromise.js). Backend opcional: PHP en `/api/` o serverless `/functions/` (elige y documenta).

**Lo que necesito en la salida (formato obligatorio):**
1) **Árbol real** del proyecto y **diagrama Mermaid `graph TD`** (IDs seguros, etiquetas en `[...]`).  
2) **Todos los archivos** en bloques de código, cada uno con:  
   - `# filename: ruta`  
   - `<!-- Propósito: … -->` en la primera línea  
   - Contenido completo y funcional  
3) **README.md** con: requisitos, instalación, build, preview, deploy, medición PSI/Lighthouse, accesibilidad (WCAG), seguridad (OWASP), PWA checklist.  
4) **PWA** completa (`site.webmanifest` + `service-worker.js` con estrategias citadas).  
5) **Optimización**: Critical CSS inline, lazy images, budgets (JS inicial ≤ 80 KB gz si procede), WebP/AVIF, split de CSS residual.  
6) **Seguridad**: CSP no permisiva, HSTS, `Referrer-Policy`, `Permissions-Policy`; saneado/CSRF si hay formularios/API.  
7) **Justificación** breve de las decisiones de rendimiento/seguridad/accesibilidad en el README.

**Notas operativas:**
- Si no puedes ver los adjuntos, **pídelos** antes de continuar.  
- Si el contenido excede el límite, **entrega en bloques**: (1) árbol+Mermaid, (2) HTMLs, (3) CSS/JS, (4) SW/manifest, (5) API/serverless, (6) README.  
- No añadas librerías no permitidas.  
- Mantén **nombres y rutas** claros y consistentes.

**Entrega ahora** la solución completa siguiendo estas reglas y el formato indicado.