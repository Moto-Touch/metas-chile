# Metas y Variable Chile

Aplicación web (archivo único `index.html`) para declarar mes a mes los supuestos de metas y variable de la fuerza de venta de Motorola Chile: portafolio e inventario por cuenta, reglas de construcción de la meta, reglas del variable MotoAgentes, importación de la Base de trabajo, checklist y bitácora.

- Datos: sistema TRADE (Supabase). La página solo llama funciones `app_*` con usuarios autenticados (Supabase Auth); sin sesión no expone nada.
- Hospedaje: GitHub Pages desde este repositorio. Cada cambio en `index.html` se publica solo.
- Acceso: usuarios creados por Motorola en Supabase Auth y habilitados en `app_usuario` (rol editor o lectura).
