# Copiloto · Supervisor

App web (GitHub Pages) para que cada supervisor de la fuerza de venta Motorola Chile vea su cartera, la ficha de cada promotor y las alertas que genera el Copiloto WhatsApp. Solo lectura más la gestión de alertas (los mismos botones que llegan por WhatsApp).

- Base: TRADE (Supabase `noskbefdrtayhwydlbfx`), mismo login que `metas-chile` (Supabase Auth, tabla `app_usuario`).
- Rol `supervisor` en `app_usuario` + fila en `copiloto_supervisor` con su `user_id` → ve solo su zona. Rol `editor` → ve todas y puede filtrar.
- RPC: `sup_cartera`, `sup_ficha`, `sup_alertas`, `sup_alerta_gestionar`, `sup_tablero`, `sup_lista`. Todo `SECURITY DEFINER`; anon no ejecuta nada.
- Pantallas: `#cartera` (2x2 por promotor), `#promotor/<id>` (30 días), `#alertas`, `#tablero`.

Datos de ejemplo (origen `ejemplo`) cargados el 16-nov-2026 para 9 promotores; se reemplazan con el piloto en seco.
