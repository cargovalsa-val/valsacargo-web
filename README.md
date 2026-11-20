# VALSA CARGO – Sitio web corporativo

Sitio institucional publicado con **GitHub Pages** en `www.valsacargo.com.co`.

| Dato | Valor |
|---|---|
| Organización | `cargovalsa-val` |
| Repositorio | `valsacargo-web` |
| Rama de publicación | `main` |
| Versión | v1.1 |

## Estructura del proyecto

```text
valsacargo-web/
├── CNAME                 → www.valsacargo.com.co
├── README.md
├── index.html
├── logovalsa.png
├── Documentos/           → PDF del Sistema de Gestión (SGS)
│   └── Politica-Objetivos-y-Alcance-del-SGS-web.pdf
└── galeria/              → Fotografías reales de la operación
    ├── operacion1.jpg
    └── ...
```

## Menú del sitio

Inicio · Servicios · Nosotros · Cobertura · **SGS** · **Galería** · Contacto · Cotizar

## Sección SGS (Sistema de Gestión y Seguridad)

Publica la documentación del Sistema Integrado de Gestión.

Documentos sugeridos: Política del SGS, Objetivos, Alcance, Política SST, Plan de Emergencias,
Reglamento de Higiene y Seguridad, Política de Calidad, Política Ambiental, Procedimientos Operativos, Certificaciones.

### Agregar un documento

1. En el repositorio, abrir la carpeta `Documentos`.
2. **Add file → Upload files** y cargar el PDF (nombre sin espacios ni tildes).
3. **Commit changes**.
4. En `index.html`, agregar una línea en la lista `SGS_DOCS` (al final del archivo):

```js
{ titulo: "Política SST", archivo: "Politica-SST.pdf" },
```

## Sección Galería

Carpeta: `galeria/`. Las fotos listadas en `GALERIA` (al final de `index.html`) que aún no existan
se ocultan automáticamente; si no hay ninguna, el sitio muestra "Próximamente".

Temas recomendados: operaciones portuarias, transporte terrestre, almacenamiento / cross docking,
operaciones internacionales y equipo humano (capacitaciones, jornadas SST, brigadas).

### Agregar fotografías

1. Abrir la carpeta `galeria` → **Add file → Upload files** → **Commit changes**.
2. Si el nombre es nuevo, agregarlo en la lista `GALERIA` de `index.html`:

```js
{ archivo: "operacion7.jpg", texto: "Consolidación de carga" },
```

Formatos: JPG, PNG o WEBP · 1200–2000 px de ancho · menos de 1 MB por imagen.

## Dominio

- Principal: `www.valsacargo.com.co`
- Raíz: `valsacargo.com.co`
- El archivo `CNAME` debe contener únicamente: `www.valsacargo.com.co`

## Publicación

Cada commit en `main` publica automáticamente el sitio en GitHub Pages (1 a 5 minutos).
Verificar en la pestaña **Actions** que el despliegue termine en verde.

## Buenas prácticas

- Nombres de archivo sin espacios ni tildes; usar guiones (`-`). GitHub distingue mayúsculas y minúsculas.
- Mantener los PDF actualizados y publicar solo información aprobada por VALSA CARGO.
- Optimizar imágenes antes de subirlas y conservar copia local.

## Roadmap

- **Fase 1 (v1.1):** sitio institucional, GitHub Pages, sección SGS, galería operacional.
- **Fase 2:** buscador de documentos SGS, descarga agrupada, certificados, PQRS, cotizador avanzado.
- **Fase 3:** portal de clientes, trazabilidad documental, dashboard logístico, Microsoft Forms, Power BI.
