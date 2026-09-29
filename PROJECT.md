# Club Penguin 2.0 (nombre pendiente)

Juego web multijugador 2D inspirado en Club Penguin, con identidad propia para evitar
problemas legales: mismo "feel" (mundo por salas, personalización, minijuegos, chat en
vivo), pero personajes, mapa, arte y lore propios.

## Concepto

Juego por osos polares con un villano pingüino. El detalle completo de diseño de
personajes, lore/historia y escenarios vive en `docs/design/`, no aquí:

- [docs/design/characters.md](docs/design/characters.md) — diseño de los osos, personalización, estilo visual
- [docs/design/lore.md](docs/design/lore.md) — lore de la isla, la semilla, el villano, elenco
- [docs/design/environment.md](docs/design/environment.md) — mapa de la isla, salas clave, estilo por zona

## Stack (propuesto, a confirmar en la doc de tech)

- **Cliente:** Phaser 3 (JS/TS)
- **Servidor de salas en tiempo real:** Colyseus (Node.js)
- **Base de datos:** PostgreSQL
- **Auth:** JWT + bcrypt
- Alternativas a evaluar/descartar explícitamente: Godot, Node puro.
- Presupuesto: cero al inicio, todo local/gratuito hasta tener MVP jugable.
- Sin plazo corto — proyecto para hacer bien, con margen para aprender.

## Equipo

- Se construye entre dos personas (autor del repo + su primo), el mismo dúo detrás
  de otros proyectos compartidos (VALORIA, inventario de bodega).

## Estado actual / próximos pasos

1. Confirmar stack final (chat "Tecnologías").
2. MVP: una sala, movimiento en tiempo real, ver a otro jugador, chat (chat
   "Desarrollo").
3. En paralelo, sin bloquear el MVP: diseño de personajes, escenarios, historia,
   UI/UX de la web (landing, login, perfil, noticias — la web del juego, no la UI
   dentro del juego).

## Cómo usar este archivo

Este archivo da contexto de producto/diseño para cualquier IA o persona que entre al
repo. Las decisiones de diseño ya tomadas (ver arriba) son fijas salvo que se diga lo
contrario explícitamente — no las reinventes ni propongas 3D, puffles, o pingüinos
como jugadores. Las cosas marcadas "por definir" siguen abiertas.
