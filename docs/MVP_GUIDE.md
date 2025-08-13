Guía para Codex – BCE Compliance Hub (MVP)

1. Objetivo

Desarrollar un hub web que permita:
• Configurar datos iniciales de la empresa.
• Detectar qué reportes de cumplimiento BCE aplica (SAPT4, SAPL2, SAPL3, SAPL4, etc.).
• Recordar y agendar entregas en Google Calendar y WhatsApp.
• Cargar insumos (Excel, CSV, PDFs).
• Generar automáticamente los reportes en la estructura y formato exigidos por el Banco Central del Ecuador.

⸻

2. Alcance del MVP
• Registro y login de usuarios con roles (admin, colaborador).
• Configuración inicial de empresa (RUC, razón social, permisos y licencias).
• Motor de reglas que asigna reportes según perfil.
• Carga manual de insumos (arrastrar y soltar).
• Generación de reportes SAP* en formato BCE (CSV, XLSX, PDF).
• Integraciones:
• Google Calendar API para agendar recordatorios.
• WhatsApp Cloud API para enviar alertas.
• Dashboard con estado de cumplimiento.

⸻

3. Arquitectura y Stack Tecnológico
• Frontend: React + Next.js (Vercel para hosting).
• Backend: Node.js (Express) o Python (FastAPI) – desplegable en Railway/Render.
• Base de Datos: Supabase (PostgreSQL) con autenticación integrada.
• Almacenamiento: Supabase Storage o AWS S3.
• Integraciones: Google API, WhatsApp Cloud API, SendGrid (opcional para email).
• Control de versiones: GitHub.

⸻

4. Flujo del MVP
1. Registro/Login (correo y contraseña, OAuth opcional).
2. Configuración inicial:
• Ingresar RUC.
• API consulta pública para permisos y licencias vigentes.
• Selección/confirmación de reportes BCE aplicables.
3. Carga de insumos (archivos anexos).
4. Generación de reportes en formatos BCE con validación de estructura.
5. Agendamiento de entregas en Google Calendar y envío de recordatorios WhatsApp.
6. Descarga de reportes listos y checklist de cumplimiento.

⸻

5. Estándares de Formato BCE
• CSV codificado en UTF-8.
• Encabezados obligatorios según anexo.
• Sin caracteres especiales fuera del set permitido.
• Campos obligatorios completados.
• Nomenclatura de archivos según formato oficial (sin espacios ni versiones).

⸻

6. Seguridad y Cumplimiento
• Encriptar datos en tránsito (HTTPS) y en reposo (AES-256).
• Control de acceso basado en roles.
• Cumplir LOPDP y normativa BCE.
• Registro de auditoría de accesos y descargas.

⸻

7. Roadmap

Fase 1 – MVP (2-4 semanas):
• Registro/login.
• Configuración inicial de empresa.
• Selección de reportes.
• Carga de insumos y generación de un reporte (ej. SAPT4).

Fase 2 – Integraciones (4-6 semanas):
• Google Calendar API.
• WhatsApp Cloud API.
• Soporte multi-reporte.

Fase 3 – Expansión (6-8 semanas):
• Validación automática de formato BCE.
• Notificaciones por email.
• Exportación masiva.
