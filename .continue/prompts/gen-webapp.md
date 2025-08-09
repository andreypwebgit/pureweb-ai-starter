---
name: Generar Web App de la Guía Copilot+Continue (Zero-Deps)
alwaysApply: false
---

## Objetivo
Construir **una Web App de documentación práctica** para ayudar a programadores a **usar GitHub Copilot + Continue en VS Code con OpenRouter (BYOK)**, basada **estrictamente** en los adjuntos disponibles del repo:
- `docs/git_hub_copilot_and_continue_integration.md`

La web **no es un sitio sobre la filosofía**; la **aplica** (Zero Dependencies / Maximum Performance) y **enseña** a implementar la integración paso a paso: instalación, configuración `config.yaml`, manejo de contexto (@Codebase/@Tree/@repo-map), solución de errores (Apply, rate limits 429), plantillas de prompts y modelos.

## Arquitectura (innegociable)
- **Frontend:** HTML5 semántico puro, **JS ES6+ vanilla**, **Tailwind v4+ vía `npx @tailwindcss/cli`** (sin CDN).
- **Sin frameworks** ni librerías externas de UI; **cero dependencias** de runtime.
- **PWA:** `site.webmanifest` + `service-worker.js` (precache + SWR para assets; network-first para HTML).
- **Accesibilidad:** WCAG 2.1 AA; foco visible, contraste, navegación por teclado, “skip link”.
- **Seguridad:** CSP restrictiva, HSTS, `Referrer-Policy`, `Permissions-Policy`. Formularios saneados si los hubiera.
- **Performance-First:** PSI objetivo ≥95 (móvil/desktop); optimiza LCP/INP/CLS; JS inicial ≤ 80KB gz (si viable).
- **SEO:** HTML semántico, `robots.txt`, `sitemap.xml`. Sin dependencias para búsqueda: **buscador local** simple (JS) sobre índice en memoria.

## Contenidos mínimos (derivados de los adjuntos)
Páginas en `/` (una sección = una página o anchor):
1. **Inicio** (qué es y para quién, CTA “Empezar ya”)
2. **Pre-requisitos** (VS Code, extensiones, cuentas, API Key)
3. **Config de Continue** (`config.yaml` + secretos `.env`; modelos OpenRouter; embeddings/reranker opcional)
4. **Contexto del repo** (Workspace Index de Copilot, `@Codebase/@Tree/@repo-map/@Folder/@File`, `.continueignore`)
5. **Flujos recomendados** (Copilot para overview/completions vs Continue para chat
