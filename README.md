# Altze Digital — sitio web multipágina

Proyecto React + Vite. Navegación con rutas reales: Inicio, Servicios, Planes, Altze Labs, Nosotros y Contacto.

## Requisitos
- Node.js 20.19+ o 22.12+
- Cuenta de Vercel

## Ejecutar localmente
1. Descomprime el ZIP.
2. Abre la carpeta `altze-web` en VS Code.
3. Abre Terminal dentro de VS Code.
4. Ejecuta `npm install`.
5. Ejecuta `npm run dev`.
6. Abre la URL local que Vite muestre (normalmente http://localhost:5173).

## Publicar en Vercel
1. Sube la carpeta del proyecto a un repositorio de GitHub.
2. En Vercel: Add New → Project → importa ese repositorio.
3. Framework Preset: Vite. Build Command: `npm run build`. Output Directory: `dist`.
4. Pulsa Deploy.
5. En Vercel → Project → Settings → Domains agrega `altzedigital.com` y `www.altzedigital.com`.
6. Sigue exactamente los registros DNS que Vercel muestre en IONOS. No borres registros MX/TXT del correo.

## Antes de publicar
- Reemplazar el logo provisional “A” por el archivo oficial de Altze. Colocar el archivo en `public/` y actualizar `Brand()` en `src/App.jsx`.
- Reemplazar `calendarUrl` en `src/App.jsx` por el enlace real de citas de Google Calendar.
- El formulario actual abre el programa de correo del visitante (mailto); para enviar desde la web sin depender del correo del visitante, conectar Formspree o una función backend y configurar antispam.
- La lista de espera de Altze Labs también usa mailto como solución provisional.
- Stripe NO está conectado. Para cobros recurrentes hay que crear productos y precios en Stripe y una integración segura de Checkout/Billing en backend o funciones serverless. Nunca pegar claves secretas en React ni en variables `VITE_`.
- Revisar textos, servicios y precios antes de hacer público el sitio. La página Planes evita publicar tarifas no confirmadas y solicita propuesta personalizada.

## Dominio y correo
Mantén el dominio en IONOS si ahí lo compraste. Conecta únicamente los registros web que Vercel indique. Conserva los MX y demás registros que utiliza tu correo `@altzedigital.com`.
