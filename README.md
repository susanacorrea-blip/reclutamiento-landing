# reclutamiento-landing

Landing estática de alto rendimiento para reclutamiento y registro en pruebas de usabilidad. HTML + CSS únicamente, sin frameworks ni JavaScript de aplicación.

## Estructura del proyecto

```
/
├── index.html
├── styles.css
├── README.md
└── assets/          (opcional: logo y recursos)
```

## Requisitos

- Navegador moderno
- Sin herramientas de build
- Sin dependencias de Node

## Despliegue en Vercel (desde GitHub)

1. **Sube el proyecto a GitHub**
   - Crea un repositorio y sube los archivos (`index.html`, `styles.css`, `README.md`, y opcionalmente `assets/`).

2. **Conecta con Vercel**
   - Entra en [vercel.com](https://vercel.com) e inicia sesión (con GitHub si lo prefieres).
   - Click en **Add New** → **Project**.
   - Importa el repositorio de GitHub que contiene este proyecto.
   - **Framework Preset:** deja "Other" o "None".
   - **Build Command:** vacío (no hay build).
   - **Output Directory:** vacío o `.` (raíz).
   - **Install Command:** vacío.
   - Despliega con **Deploy**.

3. **Dominio personalizado (subdominio usuarios.aguayo.co)**

   - En el dashboard del proyecto en Vercel: **Settings** → **Domains**.
   - Añade el dominio: `usuarios.aguayo.co`.
   - Vercel mostrará las instrucciones de DNS; para un subdominio suele pedir un **CNAME**.

4. **Configuración DNS (en tu proveedor de dominio)**

   - En el panel DNS del dominio `aguayo.co` (donde gestionas los registros):
   - Añade un registro **CNAME**:
     - **Nombre / Host:** `usuarios` (o `usuarios.aguayo.co` según cómo lo pida tu proveedor).
     - **Valor / Apunta a:** `cname.vercel-dns.com` (o el valor que indique Vercel en **Domains**).
   - Guarda los cambios. La propagación puede tardar unos minutos hasta 48 horas.
   - En Vercel, cuando el CNAME esté correcto, el dominio mostrará un estado de verificación en verde.

## Migración futura a Wagtail

- El HTML está dividido en bloques semánticos (`<header>`, `<main>`, `<section>`, `<footer>`).
- Las secciones (Hero, Formulario, Footer) están claramente separadas y pueden mapearse a bloques o snippets en Wagtail sin acoplamiento a frameworks.

## Formulario (Fillout)

Reemplaza el contenido dentro de `.fillout-embed` en `index.html` por el código de inserción (iframe o script) que proporcione Fillout. Si dejas el div actual, se mostrará el placeholder: "Aquí se cargará el formulario de registro."

## Licencia

Uso interno / proyecto Aguayo.
