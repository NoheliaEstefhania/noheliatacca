# 🌐 Contexto del Proyecto: Portafolio Académico de Nohelia Tacca Apaza

> **Documento de Contexto, Arquitectura y Registro de Planes**  
> **Fecha de creación:** Noviembre 2026  
> **Última actualización:** 4 de Noviembre de 2026 (Versión 2.0 Estable)  
> **Autora / Titular:** Nohelia Estefhania Tacca Apaza  
> **Repositorio GitHub:** [NoheliaEstefhania/noheliatacca](https://github.com/NoheliaEstefhania/noheliatacca)  
> **URL Pública en Producción:** [https://noheliaestefhania.github.io/noheliatacca/](https://noheliaestefhania.github.io/noheliatacca/)  

---

## 1. 👤 Perfil de la Autora y Objetivos

### Sobre Nohelia Tacca Apaza
- **Profesión principal:** Ingeniera de Sistemas y Contadora Pública (Universidad Nacional de San Agustín de Arequipa - UNSA, Perú).
- **Rol actual:** Docente de Lengua Quechua en el Centro de Idiomas de la UNSA.
- **Antecedentes académicos destacados:**
  - **Fulbright FLTA Fellow (2025–2026):** Docente de Quechua e investigadora visitante en **Cornell University** (Ithaca, NY, EE. UU.), Departamento de Estudios Romances y Programa de Estudios Latinoamericanos y Caribeños (LACS).
  - **Liderazgo y Voluntariado:** Miembro de **Global Shapers Community - World Economic Forum (WEF) Arequipa Hub**, Directora de Robótica Educativa en HOOP Perú, Fundadora de *Descubriendo Oportunidades* e *IA para Niños* (Nuñoa, Melgar, Puno).
  - **Reconocimientos:** Beca Fulbright FLTA, Beca CHOP+ (Embajada de EE. UU.), Aspire Leaders Program Fellow & Seed Fund Winner (Harvard/Aspire Institute), Mención Honrosa en SIMBig 2026, Grace Hopper Celebration Scholar (GHC).

### Áreas de Investigación
1. **Revitalización del Quechua Sureño** (Cusco-Collao y Puno).
2. **Procesamiento de Lenguaje Natural (NLP)** para lenguas originarias de bajos recursos morfosintácticamente complejas.
3. **Computer-Assisted Language Learning (CALL)** y analizadores morfológicos deterministas (*Paqocha Analyzer*).
4. **Cognición Corpórea (Embodied Cognition)** y Adquisición de Segundas Lenguas (SLA) vinculada a danzas y coreografías andinas tradicionales (*Kuntur Tusuy*).
5. **Humanidades Digitales Andinas**, pedagogía cultural y soberanía de datos lingüísticos.

---

## 2. 🛠️ Stack Tecnológico y Arquitectura

| Componente | Tecnología / Herramienta | Detalles |
| :--- | :--- | :--- |
| **Generador Estático** | Hugo | Versión `v0.169.0+extended` (Go static site generator) |
| **Ecosistema / Starter** | Hugo Blox Kit | Starter *Academic CV* con Tailwind CSS v4 |
| **Estilos y Diseño** | Tailwind CSS v4 | `@tailwindcss/cli`, `@tailwindcss/typography` |
| **Tema Visual Activo** | Pack `"cupcake"` | Configurado en `config/_default/params.yaml` |
| **Gestor de Paquetes** | pnpm | Node.js v22+ |
| **Control de Versiones** | Git + GitHub | Rama principal: `main` |
| **CI/CD & Despliegue** | GitHub Actions + GitHub Pages | Pipeline automatizado que despliega en ~2 min tras cada `git push` |

---

## 3. 📂 Estructura del Proyecto y Dónde Editar Cada Sección

```text
noheliatacca/
├── .docs/                             # Documentación técnica e histórico de arquitectura
│   ├── contexto_proyecto.md           # 🌟 Arquitectura, stack y registro de planes
│   └── TODO.md                        # 📋 Lista de tareas pendientes y próximos pasos
├── .github/workflows/                 # Automatizaciones de CI/CD para GitHub Actions
│   └── deploy.yml                     # Workflow oficial de compilación y despliegue a GitHub Pages
├── assets/
│   └── media/                         # Recursos gráficos principales del sitio
│       ├── icon.png                   # Favicon de la pestaña del navegador (512x512)
│       ├── sharing.png                # Imagen Open Graph para WhatsApp/LinkedIn (1200x630)
│       └── authors/                   # Fotos de perfil de la autora
│           ├── me.png                 # Foto de avatar principal (redonda)
│           ├── me0.png                # Foto alternativa
│           └── me_mh.png              # Foto en Mount Holyoke College
├── config/_default/                   # Configuración del sitio
│   ├── hugo.yaml                      # Título del sitio, baseURL y metadatos del proyecto
│   ├── params.yaml                    # Tema activo ("cupcake"), bloqueo de picker, header/footer
│   ├── menus.yaml                     # Menú superior con desplegables (Experience y Projects)
│   └── module.yaml                    # Dependencias de módulos Hugo Blox
├── content/                           # Contenido público del sitio (páginas y posts)
│   ├── _index.md                      # Portada (Bio): Avatar, datos clave, misión y botón See all research
│   ├── experience.md                  # Landing de Experience: #experience, #education, #awards, #skills, #languages
│   ├── research.md                    # Landing de Research: Colección de publicaciones en cuadrícula nativa
│   ├── events/                        # Ponencias y conferencias invitadas (10 eventos individuales)
│   │   ├── _index.md                  # Título "Invited Talks, Cultural Workshops and Academic Events"
│   │   ├── nyu-quechua/               # NYU - Quechua Language & Culture Program (Mayo 2026)
│   │   ├── mtholyoke-2026/            # Mt. Holyoke - Living Voice of the Andes (Abril 2026)
│   │   ├── cornell-acoustic-colonialism/ # Cornell - Mesa redonda Colonialismo Acústico (Abril 2026)
│   │   ├── suny-oneonta-workshop/     # SUNY Oneonta - Taller vivencial de Quechua (Marzo 2026)
│   │   ├── upenn-quechua-teaching/    # UPenn - Mesa redonda enseñanza de Quechua (Febrero 2026)
│   │   ├── suny-oneonta-fulbright/    # SUNY Oneonta - Panel Fulbright Brings the World to Us (Nov 2025)
│   │   ├── mtholyoke-2025/            # Mt. Holyoke - Living Voice of the Andes (Nov 2025)
│   │   ├── cornell-world-languages-day/ # Cornell LRC - World Language Day (Oct 2025)
│   │   ├── cornell-heritage-lectures/ # Cornell - Charlas para hablantes de herencia (2025-2026)
│   │   └── cornell-cultural-workshops/ # Cornell - Talleres culturales vivenciales (2025-2026)
│   ├── projects/                      # Proyectos comunitarios y voluntariados
│   │   └── _index.md                  # #leadership (7 chips de ancho 100%) y #volunteering (6 voluntariados)
│   ├── publications/                  # Artículos y conferencias académicas
│   │   ├── _index.md                  # Archivo de publicaciones
│   │   ├── conference-paper/index.md  # SIMBig 2026 (Mención Honrosa - Paqocha Analyzer + Mozilla Dataset)
│   │   ├── journal-article/index.md   # CILLA XI / SAIL / First Glocal (Kuntur Tusuyta Tususunchis)
│   │   └── preprint/index.md          # SSILA 2026 / SAIL / First Glocal (Paqocha RAG)
│   ├── courses/                       # Cursos de docencia (Cornell Quechua y UNSA Quechua)
│   │   ├── _index.md                  # Título "Teaching and Courses"
│   │   ├── cornell-quechua/           # Elementary Quechua I & II (Cornell University)
│   │   └── unsa-quechua/              # Quechua Sureño Inicial, Intermedio y Avanzado (UNSA)
│   └── blog/                          # Sección de opinión/ensayos (oculta de navegación por ahora)
├── data/authors/
│   └── me.yaml                        # 🌟 ARCHIVO CLAVE: Perfil, educación, experiencia, premios, lenguas (UTF-8)
├── layouts/_partials/                 # Plantillas HTML locales personalizadas
│   ├── page_links_div.html            # Renderizado seguro de botones de links con Tailwind
│   ├── functions/build_links.html     # Stub seguro para prevenir errores de Go map
│   └── hooks/head-end/
│       ├── github-button.html         # Botón de GitHub
│       ├── section-anchors.html       # Auto-scroll suave para anclas de submenús (#education, etc.)
│       └── custom-styles.html         # Normalización de tamaños de título h1 (30px / text-3xl)
├── static/
│   ├── media/projects/                # Carpeta dedicada para miniaturas/fotos de proyectos comunitarios
│   └── uploads/
│       └── resume.pdf                 # Archivo PDF descargable del CV más reciente
└── _archive/                          # Copia de seguridad de componentes demo no utilizados
```

---

## 4. 🗺️ Evolución del Proyecto: Registro de Fases y Planes Realizados

Para transformar la plantilla inicial en un portafolio académico de alta calidad adaptado al CV real de Nohelia, se ejecutaron las siguientes fases y planes de trabajo:

### Fase 1: Diagnóstico Inicial y Configuración Base (`plan-actualizacion.md`)
- **Limpieza de plantilla:** Descarte y archivado de páginas demo con shortcodes incompatibles (`fragment`, `notebook`, etc.).
- **Solución a errores de compilación:** Actualización de versiones erróneas en GitHub Actions (`actions/checkout@v4`, `setup-node@v4`) y migración a Hugo `v0.169.0` para solucionar el bug upstream de asignación a mapas nulos de Go.
- **Carga de datos primarios:** Creación del archivo de perfil `data/authors/me.yaml` con la biografía, educación universitaria (UNSA, Cornell, Chile, Colombia), experiencia docente y becas.

### Fase 2: Reestructuración de Navegación y Secciones (`plan-reestructuracion-web.md`)
- **Menús desplegables:** Organización de la barra superior en submenús lógicos en `config/_default/menus.yaml`:
  - `Experience ▾`: Enlaces internos con scroll suave a `#experience`, `#education`, `#awards`, `#skills` y `#languages`.
  - `Projects ▾`: Enlaces directos a `#leadership` (Liderazgo Comunitario) y `#volunteering` (Voluntariados).
  - Enlaces directos a `Research`, `Talks` y `Teaching`.
- **Alineación con el CV:** Reordenamiento de las secciones para colocar *Awards & Honors* antes de *Skills and Expertise*, respetando la jerarquía académica del CV.
- **Ocultamiento de Opinión:** Preservación de la sección `content/blog/` en el código pero oculta de la navegación hasta que se publiquen ensayos futuros.

### Fase 3: Separación Limpia de Bio y Research (`plan-separar-bio-research.md`)
- **Descongestión de la Portada (Bio):**
  - La portada inicial sufría de scroll infinito y duplicaba publicaciones y ponencias.
  - Se retiraron las colecciones repetidas de portada, manteniendo únicamente la presentación biográfica y la sección de misión investigadora (*📚 My Research & Mission*).
  - Al final de la misión se agregó un botón sobrio y elegante: **`See all research →`**, con estilo idéntico al botón de eventos (borde sutil, fondo limpio, sin degradados estridentes).
- **Creación de la Página Research dedicada:**
  - Creación de [`content/research.md`](file:///C:/Users/nohel/Desktop/Portafolio%20Nohelia/noheliatacca/content/research.md) utilizando el bloque nativo `collection` de Hugo Blox con vista en cuadrícula de 2 columnas (`view: article-grid`).
  - Esto aseguró que cada publicación conserve sus badges automáticos, enlaces a diapositivas, código, datasets y páginas de detalle sin romper el diseño del tema.

### Fase 4: Expansión Visual y Multimedia en Talks y Teaching
- **Charlas y Conferencias (Talks):**
  - Expansión a 10 carpetas independientes en `content/events/` correspondientes a todas las ponencias invitadas del CV (NYU, Mount Holyoke, Cornell, SUNY Oneonta, UPenn).
  - Sustitución de imágenes genéricas por fotografías reales en cada carpeta (`featured.png`).
- **Docencia (Teaching):**
  - Configuración de los cursos en `content/courses/` (*Cornell Quechua* y *UNSA Quechua*) con sus respectivos programas, marcos pedagógicos y fotos reales.
- **Normalización de Encabezados (CSS Custom):**
  - Creación de [`layouts/_partials/hooks/head-end/custom-styles.html`](file:///C:/Users/nohel/Desktop/Portafolio%20Nohelia/noheliatacca/layouts/_partials/hooks/head-end/custom-styles.html) para reducir el tamaño descomunal de fábrica (`lg:text-6xl` / 60px) en los títulos de Talks y Teaching a **`1.875rem` (30px / `text-3xl font-bold`)**, igualándolo exactamente al encabezado de *Experience* y *Research*.

### Fase 5: Rediseño de Community Leadership y Voluntariados (`plan-projects-community-leadership.md`)
- **Unificación a Ancho Completo (100%):**
  - Los primeros chips se veían angostos y excesivamente largos por estar en 2 columnas (`md:grid-cols-2`), mientras el último ocupaba todo el ancho (`col-span-2`).
  - Se cambió la cuadrícula a un flujo vertical espaciado (`space-y-6`), logrando que **todos los chips tengan el mismo ancho amplio y legible**.
- **Incorporación de Proyectos Faltantes del CV:**
  - Se agregaron los dos proyectos de Cornell University financiados por el *Language Resource Center (LRC) Grant*:
    1. *Pachamamawan kawsayninchismanta, Our Life with the Pachamama* (Dirección y recursos audiovisuales).
    2. *Intiq wawankunaq willakuyninkuna* (Colaboración pedagógica y libro digital interactivo).
- **Pastillas Elegantes para Socios y Financiamiento:**
  - Sustitución del texto gris apagado por badges redondeados con fondo suave (`bg-gray-50 dark:bg-gray-800/60 border border-gray-200`) y etiquetas en negrita con el color primario de la web (*Partner*, *Collaborators*, *Grant*).
- **Lista de Reportes en AI for Children:**
  - Apilamiento en lista vertical con enlaces individuales para los reportes de 2023, 2024, 2025 y 2026.
- **Destacado de Fechas en Voluntariados:**
  - Ubicación en alto contraste y fechas resaltadas con el color temático de la marca.

### Fase 6: Pulido de Identidad, Codificación y Tema Visual
- **Eliminación de caracteres distorsionados (Mojibake):**
  - Limpieza de `icon: ""` en `data/authors/me.yaml` para eliminar el texto residual distorsionado sobre la foto de perfil en Bio.
  - Conversión y guardado estricto en **UTF-8** de todas las tildes y caracteres especiales (*San Agustín*, *Católica*, *Medellín*, *Nuñoa*, etc.).
- **Desvinculación de Flipbook en Investigación:**
  - Corrección en `content/publications/journal-article/index.md` (*Kuntur Tusuyta*), retirando el enlace al flipbook interactivo que pertenecía al proyecto de cuentos andinos.
- **Personalización del Tema y Control de Visitantes:**
  - En `config/_default/params.yaml` se activó el tema **`"cupcake"`** por defecto.
  - Se configuró **`theme_picker: false`** para que los visitantes no puedan cambiar el tema ni vean el selector desplegable.
  - Se desactivó la barra de búsqueda innecesaria (`search: false`).
- **Actualización del CV en PDF:**
  - Carga y publicación del archivo oficial y actualizado en [`static/uploads/resume.pdf`](file:///C:/Users/nohel/Desktop/Portafolio%20Nohelia/noheliatacca/static/uploads/resume.pdf), vinculado al botón *Download CV*.

---

## 5. 🔗 Enlaces Oficiales y Recursos Clave Integrados

- **Google Scholar:** `https://scholar.google.com/citations?user=BUPCfeUAAAAJ&hl=es&oi=ao`
- **ORCID:** `https://orcid.org/0000-0002-0761-6698`
- **LinkedIn:** `https://www.linkedin.com/in/netaap/`
- **GitHub:** `https://github.com/NoheliaEstefhania`
- **Correo Institucional:** `ntacca@unsa.edu.pe`
- **Blog Quechua en Cornell:** `https://blogs.cornell.edu/quechua`
- **Plataforma Paqocha Analyzer:** `https://paqocha-analyzer.vercel.app`
- **Repositorio SIMBig 2026 ASR:** `https://quechuabase.github.io/SimBigASR2026/`
- **Dataset Mozilla Data Collective:** `https://mozilladatacollective.com/datasets/cmu60wldk00jcnq07eaxdrdl5`
- **Flipbook Heyzine (Intiq wawankunaq willakuyninkuna):** `https://heyzine.com/flip-book/c4324412e8.html`
- **Videos del Proyecto Pachamama (Cornell LRC):** `https://blogs.cornell.edu/quechua/resources/videos/`
- **Video Testimonial CHOP+ (YouTube):** `https://youtu.be/Q3oQh1f0np8`
- **World Economic Forum - Arequipa Hub:** `https://initiatives.weforum.org/arequipa-hub/overview`

---

## 6. 🚀 Flujo de Trabajo para Futuras Actualizaciones

### Probar cambios en tu computadora (Local)
Abre una terminal PowerShell en la carpeta del proyecto y ejecuta:
```powershell
hugo server
```
Abre en tu navegador: **`http://localhost:1313/noheliatacca/`**  

### Publicar cambios en internet (GitHub Pages)
```powershell
git add .
git commit -m "feat: descripción breve de lo que modificaste"
git push origin main
```
El pipeline de GitHub Actions compilará y desplegará automáticamente la actualización en ~2 minutos en:  
👉 **`https://noheliaestefhania.github.io/noheliatacca/`**
