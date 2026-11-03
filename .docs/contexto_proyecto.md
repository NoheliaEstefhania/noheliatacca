# 🌐 Contexto del Proyecto: Portafolio Académico de Nohelia Tacca Apaza

> **Documento de Contexto y Arquitectura**  
> **Fecha de creación:** Noviembre 2026  
> **Autora / Titular:** Nohelia Estefhania Tacca Apaza  
> **Repositorio GitHub:** [NoheliaEstefhania/noheliatacca](https://github.com/NoheliaEstefhania/noheliatacca)  
> **URL Pública en Producción:** [https://noheliaestefhania.github.io/noheliatacca/](https://noheliaestefhania.github.io/noheliatacca/)  

---

## 1. 👤 Perfil de la Autora y Objetivos

### Sobre Nohelia Tacca Apaza
- **Profesión principal:** Ingeniera de Sistemas y Contadora Pública (UNSA, Perú).
- **Rol actual:** Docente de Lengua Quechua en el Centro de Idiomas de la Universidad Nacional de San Agustín de Arequipa (UNSA).
- **Antecedentes académicos destacados:**
  - **Fulbright FLTA Fellow (2025–2026):** Docente de Quechua e investigadora visitante en **Cornell University** (Ithaca, NY, EE. UU.), Departamento de Estudios Romances y LACS (concluido en mayo de 2026).
  - **Liderazgo y Voluntariado:** Miembro activa del **World Economic Forum (WEF) - Arequipa Hub** (Global Shapers), Directora de Robótica Educativa en HOOP Perú, Fundadora de *Descubriendo Oportunidades* e *IA para Niños* (Nuñoa, Puno).
  - **Reconocimientos:** Beca Fulbright FLTA, Beca CHOP+ (Embajada de EE. UU.), Aspire Leaders Program Fellow & Seed Fund Winner (Harvard/Aspire Institute), Mención Honrosa en SIMBig 2026, Grace Hopper Celebration Scholar (GHC).

### Áreas de Investigación
1. **Revitalización del Quechua Sureño** (Cusco-Collao / Puno).
2. **Procesamiento de Lenguaje Natural (NLP)** para lenguas originarias de bajos recursos.
3. **Computer-Assisted Language Learning (CALL)** y analizadores morfológicos deterministas.
4. **Cognición Corpórea (Embodied Cognition)** y Adquisición de Segundas Lenguas (SLA) vinculada a danzas andinas tradicionales (*Kuntur Tusuy*).
5. **Humanidades Digitales Andinas** y soberanía de datos lingüísticos.

---

## 2. 🛠️ Stack Tecnológico y Arquitectura

| Componente | Tecnología / Herramienta | Detalles |
| :--- | :--- | :--- |
| **Generador Estático** | Hugo | Versión `v0.169.0+extended` (Go static site generator) |
| **Ecosistema / Tema** | Hugo Blox Kit | Starter *Academic CV* con Tailwind CSS v4 |
| **Estilos** | Tailwind CSS v4 | `@tailwindcss/cli`, `@tailwindcss/typography` |
| **Gestor de Paquetes** | pnpm | Node.js v22+ |
| **Control de Versiones** | Git + GitHub | Rama principal: `main` |
| **CI/CD & Despliegue** | GitHub Actions + GitHub Pages | Despliegue 100% automático al hacer `git push` |

---

## 3. 📂 Estructura del Proyecto y Dónde Editar Cada Sección

```text
noheliatacca/
├── .docs/                             # Documentación interna del proyecto (este archivo)
├── .github/workflows/                 # Automatizaciones de CI/CD para GitHub Actions
│   ├── deploy.yml                     # Workflow principal de despliegue a GitHub Pages
│   └── build.yml                      # Script de compilación de Hugo, Node y Tailwind
├── assets/
│   └── media/                         # Recursos gráficos principales del sitio
│       ├── icon.png                   # Favicon de la pestaña del navegador (512x512)
│       ├── sharing.png                # Imagen Open Graph para WhatsApp/LinkedIn (1200x630)
│       └── authors/                   # Fotos de perfil de la autora
│           ├── me.png                 # Foto de avatar principal (redonda)
│           ├── me0.png                # Foto alternativa
│           └── me_mh.png              # Foto en Mount Holyoke College
├── config/_default/                   # Configuración del sitio
│   ├── hugo.yaml                      # Título del sitio, baseURL y ajustes de internacionalización
│   ├── params.yaml                    # Identidad del sitio, SEO, metadatos, temas y colores
│   ├── menus.yaml                     # Enlaces del menú de navegación superior
│   └── module.yaml                    # Dependencias de módulos Hugo Blox
├── content/                           # Contenido público del sitio (páginas y posts)
│   ├── _index.md                      # Estructura y bloques de la página de inicio (Landing Page)
│   ├── experience.md                  # Página de experiencia laboral y habilidades
│   ├── events/                        # Ponencias y conferencias invitadas
│   │   └── example/index.md           # Taller en SUNY Oneonta, charlas en Mt. Holyoke y NYU
│   ├── projects/                      # Proyectos de investigación tecnológica
│   │   ├── pandas/index.md            # Paqocha Analyzer (Analizador morfológico en Vercel)
│   │   ├── pytorch/index.md           # Paqocha RAG (Modelo de traducción español-quechua)
│   │   └── scikit/index.md            # Kuntur Tusuy (Danza y adquisición del Quechua)
│   └── publications/                  # Trabajos y ponencias presentadas en conferencias
│       ├── conference-paper/index.md  # SIMBig 2026 (Mención Honrosa - Paqocha Analyzer)
│       ├── journal-article/index.md   # CILLA XI / SAIL 2026 / First Glocal (Kuntur Tusuy)
│       └── preprint/index.md          # SSILA / SAIL 2026 / First Glocal (Paqocha RAG)
├── data/authors/
│   └── me.yaml                        # 🌟 ARCHIVO CLAVE: Datos de perfil, biografía, affiliations,
│                                      # redes (Google Scholar, ORCID), educación, experiencia y premios
├── layouts/_partials/                 # Plantillas HTML locales personalizadas
│   ├── page_links_div.html            # Renderizado seguro de botones de links con Tailwind
│   └── functions/build_links.html     # Stub seguro para prevenir errores de Go map
├── static/uploads/
│   └── resume.pdf                     # Archivo PDF descargable del CV
├── _archive/                          # Copia de seguridad de componentes demo no utilizados
│   ├── blog/                          # Posts demo que utilizaban shortcodes no disponibles
│   ├── courses/                       # Cursos de ejemplo
│   └── slides/                        # Presentaciones interactivas demo en Reveal.js
└── hugoblox.yaml                      # Configuración de compilación para Hugo Blox (v0.169.0)
```

---

## 4. 🔗 Enlaces Oficiales y Recursos Clave Integrados

- **Google Scholar:** `https://scholar.google.com/citations?user=BUPCfeUAAAAJ&hl=es&oi=ao`
- **ORCID:** `https://orcid.org/0000-0002-0761-6698`
- **LinkedIn:** `https://www.linkedin.com/in/netaap/`
- **GitHub:** `https://github.com/NoheliaEstefhania`
- **Correo Institucional:** `ntacca@unsa.edu.pe`
- **Blog Quechua en Cornell:** `https://blogs.cornell.edu/quechua`
- **Plataforma Paqocha Analyzer:** `https://paqocha-analyzer.vercel.app`
- **Repositorio SIMBig 2026 ASR:** `https://quechuabase.github.io/SimBigASR2026/`
- **Libro Digital del Proyecto (Flipbook Heyzine):** `https://heyzine.com/flip-book/c4324412e8.html`
- **Video Testimonial CHOP+ (YouTube):** `https://youtu.be/Q3oQh1f0np8`
- **World Economic Forum - Arequipa Hub:** `https://initiatives.weforum.org/arequipa-hub/overview`

---

## 5. 🚀 Flujo de Trabajo Cotidiano

### Probar en tu computadora (Local)
Abre PowerShell en la carpeta del proyecto y ejecuta:
```powershell
hugo server
```
Abre en tu navegador: **`http://localhost:1313/`**  
*(Cualquier cambio que guardes en los archivos se reflejará automáticamente en vivo sin necesidad de recargar).*

### Publicar cambios en internet
Una vez que estés conforme con tus modificaciones locales:
```powershell
git add .
git commit -m "feat: descripción breve de lo que modificaste"
git push origin main
```
El pipeline de GitHub Actions se activará de forma **100% automática** y desplegará tus cambios en **1 a 2 minutos** en:
👉 `https://noheliaestefhania.github.io/noheliatacca/`

---

## 6. 🛠️ Historial de Soluciones y Registro Técnico

Durante la configuración inicial y personalización del sitio se resolvieron los siguientes retos técnicos:

1. **Shortcodes incompatibles de la plantilla demo:**
   - *Problema:* Las carpetas de ejemplo `content/slides/`, `content/courses/` y `content/blog/` utilizaban shortcodes de Reveal.js (`fragment`, `cards`, `notebook`, `embed`) no incluidos en el kit base gratuito de Hugo Blox, bloqueando el build.
   - *Solución:* Se migraron todos los contenidos de demostración a `_archive/` (e ignorados en `.gitignore`), manteniendo el árbol de contenido limpio con el trabajo real de Nohelia.

2. **Versiones inválidas en GitHub Actions:**
   - *Problema:* La plantilla original contenía workflows con referencias a `actions/checkout@v6` y `setup-node@v6` (versiones que no existen en el catálogo de GitHub Actions).
   - *Solución:* Se ajustaron a las versiones estables oficiales (`@v4`).

3. **Regresión `SetInMap: assignment to entry in nil map` de Hugo v0.162.0:**
   - *Problema:* El archivo `hugoblox.yaml` tenía fijado `hugo_version: '0.162.0'`, la cual contenía un bug en Go que provocaba un fallo fatal al renderizar listas de enlaces en páginas de eventos y publicaciones.
   - *Solución:* 
     - Se actualizó `hugoblox.yaml` y `netlify.toml` a **`0.169.0`**.
     - Se crearon plantillas de override locales en `layouts/_partials/page_links_div.html` y `layouts/_partials/functions/build_links.html` que aíslan y blindan el renderizado de botones contra cualquier cambio upstream de Hugo Blox.
