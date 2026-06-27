# 💳 Next.js Subscription Payments Starter

Plantilla profesional para desarrollar aplicaciones **SaaS con suscripciones** utilizando **Next.js**, **Supabase** y **Stripe**.

Este proyecto proporciona una base sólida para implementar autenticación de usuarios, gestión de suscripciones, procesamiento de pagos y sincronización automática entre la base de datos y Stripe.

> **Nota:** Este proyecto ha sido descontinuado y reemplazado por el nuevo **Next.js SaaS Starter**, aunque sigue siendo una excelente referencia para aprender cómo integrar pagos recurrentes con Stripe y Supabase.

---

# ✨ Características

* 🔐 Autenticación segura mediante Supabase.
* 👤 Gestión completa de usuarios.
* 🗄 Base de datos PostgreSQL administrada por Supabase.
* 💳 Integración con Stripe Checkout.
* 📦 Portal de clientes de Stripe.
* 🔄 Sincronización automática de planes y suscripciones.
* ⚡ Webhooks para actualizar el estado de pagos.
* ☁️ Preparado para desplegar en Vercel.
* 🚀 Arquitectura moderna basada en Next.js.

---

# 🛠 Tecnologías utilizadas

* Next.js
* React
* TypeScript
* Supabase
* PostgreSQL
* Stripe
* Tailwind CSS
* Vercel
* PNPM

---

# 📁 Estructura del proyecto

```text
Saas-Stripe/
│
├── app/
├── components/
├── pages/
├── public/
├── styles/
├── supabase/
├── utils/
├── package.json
├── next.config.js
└── README.md
```

---

# ⚙️ Requisitos

Antes de comenzar instala:

* Node.js 18 o superior
* PNPM
* Docker (opcional para Supabase local)
* Cuenta en Supabase
* Cuenta en Stripe
* Cuenta en Vercel

Verifica la instalación:

```bash
node -v
pnpm -v
```

---

# 🚀 Instalación

## 1. Clonar el repositorio

```bash
git clone https://github.com/isairey/Saas-Stripe.git
```

Entrar al proyecto:

```bash
cd Saas-Stripe
```

---

## 2. Instalar dependencias

```bash
pnpm install
```

---

# 🔐 Configuración de Supabase

Crear un nuevo proyecto en Supabase.

Configurar las variables de entorno correspondientes:

```env
NEXT_PUBLIC_SUPABASE_URL=

NEXT_PUBLIC_SUPABASE_ANON_KEY=

SUPABASE_SERVICE_ROLE_KEY=
```

Inicializar la base de datos utilizando las migraciones del proyecto.

---

# 💳 Configuración de Stripe

Crear una cuenta en Stripe y habilitar el modo de pruebas.

Agregar las siguientes variables:

```env
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=

STRIPE_SECRET_KEY=

STRIPE_WEBHOOK_SECRET=
```

Crear un Webhook apuntando a:

```text
https://tu-dominio.com/api/webhooks
```

Seleccionar los eventos relacionados con:

* Checkout
* Productos
* Precios
* Suscripciones
* Clientes

---

# ▶️ Ejecutar el proyecto

Iniciar el servidor de desarrollo:

```bash
pnpm dev
```

Abrir en el navegador:

```
http://localhost:3000
```

---

# 🖥 Desarrollo local con Supabase

Si deseas trabajar completamente de forma local:

Copiar los archivos:

```text
.env.local.example → .env.local

.env.example → .env
```

Iniciar Supabase:

```bash
pnpm supabase:start
```

Consultar el estado:

```bash
pnpm supabase:status
```

Vincular el proyecto:

```bash
pnpm supabase:link
```

Actualizar la base de datos:

```bash
pnpm supabase:push
```

---

# 🔄 Migraciones

Generar migraciones:

```bash
pnpm supabase:generate-migration
```

Actualizar tipos TypeScript:

```bash
pnpm supabase:generate-types
```

Restablecer la base de datos:

```bash
pnpm supabase:reset
```

---

# 🎯 Probar Webhooks de Stripe

Iniciar sesión:

```bash
pnpm stripe:login
```

Escuchar eventos:

```bash
pnpm stripe:listen
```

Esto generará un Webhook Secret que deberá agregarse al archivo `.env.local`.

---

# 💳 Productos y Suscripciones

El proyecto permite crear automáticamente:

* Productos
* Planes mensuales
* Planes anuales
* Clientes
* Suscripciones

Toda la información se sincroniza automáticamente con Supabase mediante Webhooks.

---

# 🚀 Despliegue

La aplicación está preparada para desplegarse fácilmente en:

* Vercel
* Supabase
* Stripe

Una vez configuradas las variables de entorno solo será necesario realizar un nuevo despliegue.

---

# 🔑 Variables de entorno

Ejemplo:

```env
NEXT_PUBLIC_SITE_URL=

NEXT_PUBLIC_SUPABASE_URL=

NEXT_PUBLIC_SUPABASE_ANON_KEY=

SUPABASE_SERVICE_ROLE_KEY=

NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=

STRIPE_SECRET_KEY=

STRIPE_WEBHOOK_SECRET=
```

---

# 📱 Compatibilidad

* Windows
* Linux
* macOS

Navegadores compatibles:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

---

# 📈 Ventajas del proyecto

* Arquitectura moderna.
* Código escalable.
* Integración sencilla con Stripe.
* Gestión automática de suscripciones.
* Base de datos administrada por Supabase.
* Autenticación segura.
* Fácil despliegue en Vercel.
* Preparado para producción.

---

# 👨‍💻 Desarrollador

**Isai Reyes**

Proyecto basado en la plantilla oficial **Next.js Subscription Payments Starter**, desarrollada por el equipo de Vercel para implementar sistemas de suscripciones utilizando Next.js, Stripe y Supabase.

---

# 📄 Licencia

Este proyecto se distribuye bajo la licencia correspondiente del repositorio original y puede utilizarse como base para aplicaciones SaaS con pagos recurrentes.
