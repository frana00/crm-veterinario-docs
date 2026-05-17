# CRM Veterinario — Sistema de Gestión Integral

> Plataforma web full-stack desarrollada desde cero para la gestión operativa y financiera de clínicas veterinarias. Proyecto en producción.
>
>
> ---
>
> ## 🧩 Descripción
>
> Sistema de gestión integral para clínicas veterinarias que centraliza fichas clínicas, agenda, cobros y reportes financieros en una sola plataforma. Diseñado con arquitectura mobile-first y desplegado en producción.
>
> Este repositorio contiene **documentación pública** del proyecto (arquitectura, capturas, stack técnico). El código fuente es privado.
>
> ---
>
> ## ⚙️ Stack Técnico
>
> | Capa | Tecnología |
> |---|---|
> | Frontend | React 18 + TypeScript + Vite |
> | Backend / DB | Supabase (PostgreSQL) |
> | Auth | Supabase Auth |
> | Deploy | Vercel |
> | Pagos | Flow.cl |
> | Calendario | Google Calendar API |
> | PDF | Generación automática de documentos clínicos |
>
> ---
>
> ## 🗂️ Módulos del Sistema
>
> ### Operación
> - **Dashboard** — resumen financiero del mes, alertas de pendientes y última actividad
> - - **Agenda / Disponibilidad** — calendario semanal integrado con Google Calendar
>   - - **Revisar Citas** — seguimiento de atenciones pendientes de cobro
>    
>     - ### Gestión
>     - - **Fichas Clínicas** — registro de pacientes con historial de atenciones
>       - - **Clientes y Mascotas** — base de datos con búsqueda y filtros
>         - - **Consentimientos** — generación de documentos PDF automáticos
>           - - **Órdenes de Examen** — creación y seguimiento de órdenes de laboratorio
>             - - **Especies y Servicios** — catálogo configurable
>              
>               - ### Finanzas
>               - - **Vouchers** — historial de atenciones con estados (Pendiente, Enviado, Parcial, Pagado)
>                 - - **Presupuestos** — cotizaciones enlazadas a fichas clínicas
>                   - - **Boletas** — registro de pagos recibidos
>                     - - **Links de Pago** — integración con Flow.cl para cobro remoto
>                      
>                       - ### Exportaciones
>                       - - Exportación de clientes, mascotas, fichas y vouchers en formatos reutilizables
>                        
>                         - ---
>
> ## 🖼️ Capturas de Pantalla
>
> > Las capturas muestran la interfaz real de la aplicación en producción. Los datos personales han sido anonimizados.
> >
> > ### Dashboard principal
> > ![Dashboard](screenshots/dashboard.png)
> >
> > ### Gestión de Clientes
> > ![Clientes](screenshots/clientes.png)
> >
> > ### Vouchers / Historial de cobros
> > ![Vouchers](screenshots/vouchers.png)
> >
> > ### Formulario — Nuevo Cliente
> > ![Nuevo Cliente](screenshots/nuevo-cliente.png)
> >
> > ---
> >
> > ## 🏗️ Arquitectura
> >
> > ```
> > Usuario
> >   └── React (Vite) — Frontend SPA
> >         ├── Supabase Client — Auth + DB (PostgreSQL)
> >         ├── Google Calendar API — Disponibilidad
> >         ├── Flow.cl API — Pasarela de pagos
> >         └── Vercel — Deploy + Edge Functions
> > ```
> >
> > **Modelo de datos principal:**
> > - `clientes` → `mascotas` → `fichas_clinicas`
> > - - `fichas_clinicas` → `vouchers` → `pagos`
> >   - - `presupuestos` → `servicios`
> >     - - `consentimientos` (PDF generado automáticamente)
> >      
> >       - ---
> >
> > ## ✨ Características Destacadas
> >
> > - **Arquitectura mobile-first** — diseñada para uso desde dispositivos móviles en clínica
> > - - **Dashboard financiero en tiempo real** — resumen del mes con alertas de vouchers pendientes
> >   - - **Generación de PDF automática** — consentimientos y órdenes de examen sin intervención manual
> >     - - **Integración Google Calendar** — sincronización de disponibilidad de la doctora
> >       - - **Cobro remoto con Flow.cl** — links de pago enviados directamente a tutores
> >         - - **Exportación de datos** — descarga de registros en formato estructurado
> >          
> >           - ---
> >
> > ## 👩‍💻 Desarrollado por
> >
> > **Francisca Illanes** — Ingeniera Informática (UNIR) | Máster en Big Data (en curso)
> >
> > [![LinkedIn](https://img.shields.io/badge/LinkedIn-mariaillanes-blue)](https://linkedin.com/in/mariaillanes)
> > [![GitHub](https://img.shields.io/badge/GitHub-frana00-black)](https://github.com/frana00)
> > 
