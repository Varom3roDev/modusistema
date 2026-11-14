# WIKI: Modusistema (Web Corporativa, CRM RRHH, Automatizaciones y Flujo de Caja)

> **Última Actualización:** 2026-11-14  
> **Ruta Principal:** `D:\Modusistema`  
> **Subproyecto Web:** `D:\Modusistema\Pagina_Web`  
> **Stack Tecnológico:** HTML5 Semántico, Tailwind CSS, JavaScript Vanilla, PHP 8.1 (GoDaddy cPanel), Base64 Data URIs, Python (`openpyxl`), React/Vite  
> **Cliente / Contraparte:** Modusistema, C.A.  
> **Atención Principal:** Anna Meinhard (Gerencia General)  
> **Arquitectura & Autor:** WikiForge para Víctor (Ecosistema J.A.R.V.I.S.)

---

## 1. Resumen Ejecutivo y Propósito

**Modusistema, C.A.** es la corporación líder en Venezuela (con más de 38 años de trayectoria, showroom en Las Mercedes, Caracas, y planta industrial en Mariche) especializada en arquitectura interior, mobiliario corporativo de alta gama y sillería ergonómica. Es el **Distribuidor Autorizado en exclusiva de MillerKnoll** en el país (abarcando las marcas globales **Herman Miller, Knoll, Trekin, Virco y Mohawk Group**).

El repositorio `D:\Modusistema` centraliza todo el activo digital, comercial y de automatización operativa de la empresa, dividido en tres grandes frentes:

1. **Vitrina Digital y Experiencia de Marca (`D:\Modusistema\Pagina_Web`):**  
   Modernización integral de la plataforma web corporativa, sustituyendo el sitio web previo (construido sobre un tema pesado de WordPress con constructores lentos) por una solución ultraligera, elegante, en **Modo Claro**, con carrusel de video interactivo, catálogo digital, cotizador conectado a WhatsApp y un **panel administrativo privado (Backoffice)** para Blog y Podcast.
2. **Consultoría Comercial y Preventa (`GUIA_PREVENTA_IMPORTACIONES.md`):**  
   Estrategia desarrollada por Víctor para mitigar el stock congelado por "apartados fantasma", estructuración de anticipos comerciales (30/70) y control de rotación para importaciones marítimas de largo tránsito (90 a 180 días).
3. **Suite de Automatización Financiera y Flujo de Caja (`Modusistema Automatizaciones`):**  
   Modelos en Python (`openpyxl`) y libros de cálculo interconectados (Nómina RRHH, Cuentas por Cobrar, Cuentas por Pagar y Tesorería) para el monitoreo de liquidez de la empresa.

---

## 2. Documentación Detallada: `D:\Modusistema\Pagina_Web`

La carpeta `Pagina_Web` contiene el desarrollo completo del nuevo portal web corporativo y su propuesta comercial de modernización.

### 2.1. Arquitectura y Experiencia Visual (Front-End)
* **Diseño en Modo Claro:** Enfoque visual corporativo, luminoso, sobrio y de alto contraste, alineado con las directrices internacionales de MillerKnoll.
* **Hero Cinematográfico:** Cabecera con carrusel de videos de alta definición de la **Silla Aeron** de Herman Miller y la **Eames Lounge Chair & Ottoman**, con microinteracciones sensibles al cursor.
* **Modusistema en Números:** Animación fluida de conteo progresivo activada al entrar en el campo visual del usuario (+38 años de servicio, +170.000 m² equipados, +11.000 proyectos ejecutados, 75% relaciones a largo plazo).
* **Catálogo Estructurado:** Exhibición por fichas técnicas de puestos operativos (S-AO, SMS), oficinas ejecutivas, sillería ergonómica y líneas educativas Virco.
* **Planificador / Cotizador Interactivo:** Widget corporativo que permite a empresas y arquitectos configurar su requerimiento (tipo de proyecto y escala) y canalizarlo automáticamente hacia el WhatsApp oficial (`+58 412 230.87.25`) y correos de ventas.
* **Footer Institucional:** Información real del showroom en Las Mercedes (Torre UNO, Calle Orinoco), teléfonos de contacto directos (`tel:+584122308725` y `tel:+582129930721`) e iconografía vectorial en SVG nativo para redes sociales (Instagram, LinkedIn, Facebook, Pinterest, X, WhatsApp).

### 2.2. Módulo Administrativo Privado (CMS para Blog y Podcast)
Área interna privada diseñada para que el equipo de mercadeo y comunicaciones publique contenidos con 100% de autonomía técnica:
* **Ubicación Técnica:** Subcarpeta privada `modusistema.com/admin` dentro del hosting de GoDaddy (evita trámites de DNS externos y hereda el certificado SSL automáticamente).
* **Control de Acceso:** Login protegido por usuario y contraseña encriptada mediante PHP (`password_hash`).
* **Gestor de Blog:** Creación, edición y categorización de artículos, entrevistas a arquitectos y notas de prensa con carga de imágenes optimizadas.
* **Gestor de Podcasts:** Módulo multimedia para subir episodios de audio (`.mp3`) o incrustar reproductores desde Spotify, YouTube o Apple Podcasts con notas del episodio.

### 2.3. Infraestructura de Servidores, Dominio y Correo
* **Hosting Web:** **GoDaddy.com, LLC** (IP: `107.180.41.38`, servidor Apache con PHP 8.1.34, soporte MySQL/MariaDB y SQLite).
* **Dominio & DNS:** Registrado en **Network Solutions, LLC** (servidores `ns83.worldnic.com` y `ns84.worldnic.com`), apuntando por registro A al hosting de GoDaddy.
* **Servicio de Correo:** Operado independientemente en **Microsoft 365 / Outlook** (`modusistema-com.mail.protection.outlook.com`). Las modificaciones al sitio web en GoDaddy no afectan en ningún momento los correos corporativos.

---

## 3. Inventario de Archivos Clave en `Pagina_Web`

| Archivo / Ruta | Tipo de Documento | Descripción y Función |
| :--- | :--- | :--- |
| `index.html` | Archivo Principal | Página web oficial activa con la versión más reciente en modo claro, cotizador interactivo y assets vinculados. |
| `propuesta_14_documento_unico.html` | HTML Monolítico | Archivo 100% autosuficiente (~22.7 MB) con todas las imágenes, logos y los 2 videos MP4 embebidos en Base64 Data URIs. Abre en cualquier navegador sin dependencias externas. |
| `propuesta_14_modo_oscuro_claro.html` | Versión Base | Prototipo iterativo que sirvió de base para la consolidación de componentes y estilos. |
| `PROPUESTA_ECONOMICA_MODUSISTEMA.md` | Propuesta Comercial | Documento formal de "Alcance y Presupuesto" dirigido a Anna Meinhard con el desglose de $490 USD. |
| `PROPUESTA_ECONOMICA_MODUSISTEMA.pdf` | Documento PDF | PDF ejecutivo de 2 páginas exactas, sin espacios vacíos ni logos, listo para entrega o impresión formal. |
| `GLOSARIO_TECNICO.md` | Glosario de Términos | Explicación sencilla de 18 términos tecnológicos y de mobiliario (Front-End, CMS, WPO, SEO, S-AO, SMS, etc.). |
| `medios/` | Carpeta de Assets | Fotografías institucionales en alta definición, logotipos de marcas y catálogos de producto. |
| `video/` | Carpeta Multimedia | Videos cinemáticos en MP4 de la Silla Aeron (`silla_Aeron.mp4`) y la Eames Lounge Chair (`Eames_Lounge_and_Ottoman.mp4`). |
| `contenido/` | Respaldo del Sitio Previo | Extracción completa en formato JSON y HTML del sitio WordPress original de Modusistema (+60 páginas, +50 artículos de blog y proyectos). |

---

## 4. Resumen Comercial y Presupuesto Aprobado para la Web

| Módulo del Proyecto | Alcance de Trabajo | Monto (USD) |
| :--- | :--- | :---: |
| **Módulo 1: Reingeniería Web, UI/UX & Front-End** | Rediseño integral en modo claro, catálogo de productos, cotizador interactivo, carrusel de video y 100% responsive. | **$ 260** |
| **Módulo 2: Optimización Técnica (WPO) y SEO Base** | Limpieza de código obsoleto anterior, compresión de activos, máxima velocidad en GoDaddy y metadatos. | **$ 90** |
| **Módulo 3: Administrador Privado (Blog & Podcast)** | Backend ligero y seguro con login, gestor de artículos de blog y módulo de audio/video para podcasts. | **$ 140** |
| **Módulo 4: Despliegue, Soporte y Capacitación** | Instalación en servidor de GoDaddy, capacitación al personal de mercadeo y 30 días de garantía técnica. | **Cortesía / Incluido** |
| **TOTAL INVERSIÓN** | **Solución completa llave en mano** | **`$ 490 USD`** |

* **Esquema de Pago:** 50% de anticipo ($ 245 USD) al inicio y 50% restante ($ 245 USD) contra entrega final y capacitación.
* **Tiempo Estimado de Entrega:** 4 a 6 semanas.
* **Delimitación de Alcance:** El desarrollador provee toda la arquitectura, código, maquetación, CMS y optimización. Modusistema suministra la redacción de textos publicitarios, artículos editoriales y pistas de audio para el podcast.

---

## 5. Glosario Rápido de Mobiliario Propio de Modusistema

* **Sistema S-AO (Sistema Action Office):**  
  Estaciones de trabajo modulares basadas en **paneles y mamparas divisorias** (inspiradas en Herman Miller y fabricadas localmente por Modusistema). Diseñadas para configuraciones que requieren privacidad visual y acústica, con canalización oculta de cableado eléctrico y de red a nivel de rodapié.
* **Sistema SMS (Sistema Modular de Superficies):**  
  Línea de escritorios inteligentes, **abiertos y diáfanos tipo *benching*** (para espacios de trabajo colaborativo *open space* sin paneles divisorios intermedios). Diseño y fabricación 100% venezolana con tomas de corriente y datos accesibles sobre la superficie.

---

## 6. Componentes del Ecosistema Fuera de la Web

Para referencia integral de Víctor y J.A.R.V.I.S.:

| Módulo / Archivo | Ubicación | Función Técnica |
| :--- | :--- | :--- |
| `GUIA_PREVENTA_IMPORTACIONES.md` | `D:\Modusistema\` | Protocolo comercial para la Gerencia General sobre mitigación de apartados fantasma y política de anticipos. |
| `Modusistema Automatizaciones\Estrategia.txt` | `D:\Modusistema\` | Lineamientos estratégicos de digitalización y optimización de procesos. |
| `Modusistema Automatizaciones\Propuesta Estratégica.txt` | `D:\Modusistema\` | Oferta de servicios para tableros de control y automatización departamental. |
| `Simulacro_Flujo_Caja\generar_simulacro_excel.py` | `D:\Modusistema\` | Generador Python de hojas de cálculo interconectadas de tesorería y nómina. |
| `Simulacro_Flujo_Caja\Master_Flujo_de_Caja_Modusistema.xlsx` | `D:\Modusistema\` | Libro consolidado de proyección y control de liquidez semanal/mensual. |
