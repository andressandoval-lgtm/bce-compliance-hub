 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index 856d1bad8dfb7f9940e9445817fe5343f9b69ff1..645c255f339323cb21913b1a5243d4e6a8d5b995 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,28 @@
 # bce-compliance-hub
 Plataforma web para entidades financieras, fintechs y agregadores de pagos que deben cumplir con reportes del BCE. Integra calendario y WhatsApp para recordatorios, permite cargar insumos y genera reportes en formato y estructura exigidos por la normativa.
+
+## Clonado del repositorio
+
+```bash
+git clone https://github.com/<usuario>/bce-compliance-hub.git
+cd bce-compliance-hub
+```
+
+## Instalación de dependencias
+
+Desde la carpeta `frontend/`:
+
+```bash
+cd frontend
+npm install
+```
+
+## Ejecución del servidor
+
+```bash
+npm run dev
+```
+
+## Despliegue
+
+En servicios de despliegue (por ejemplo, Vercel) configure el directorio raíz como `frontend/`.
 
EOF
)
