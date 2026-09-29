# Convenciones del proyecto

## Idioma

Todo lo relacionado con código se maneja en **inglés**: nombres de archivos,
variables, funciones, ramas (branches) y mensajes de commit.

La única excepción es el **contenido** de la documentación (lore, personajes,
escenarios, README, este mismo archivo): se escribe en **español**. Los nombres
de los archivos de documentación, sin embargo, también van en inglés
(`docs/design/lore.md`, no `docs/design/historia.md`).

## Estrategia de ramas (Git Flow)

- `main` — versión estable. Solo recibe merges desde `develop` o `hotfix/*`,
  vía Pull Request en GitHub, o commits directos desde `main` si se trata de docs de diseño .
- `develop` — rama de integración principal. Todo el trabajo en curso converge
  acá, vía Pull Request en GitHub.
- `feature/*` — una funcionalidad de código. Nace de `develop`, muere al
  mergearse a `develop` (PR en GitHub).
- `hotfix/*` — arreglo urgente sobre `main`, luego se mergea también a
  `develop` para no perderlo (ambos vía PR).

Nombres de rama en **kebab-case** e inglés, con prefijo según el tipo:
`feature/room-movement`, `hotfix/chat-crash`.

## Documentación: ¿rama o commit directo?

- **Docs de diseño** (`docs/design/`: lore, characters, environment): no
  necesitan rama propia. Se commitea directo a `main`. No tocan código, así
  que no hay riesgo de conflicto.
- **Docs técnicos** (arquitectura, decisiones de stack) que nacen junto con
  una feature de código: van dentro de la misma rama `feature/*` que
  documentan, no aparte.


## Mensajes de commit (Conventional Commits + extensión propia)

Formato: `tipo: descripción corta en inglés, imperativo`

| Tipo          | Uso                                                        |
|---------------|-------------------------------------------------------------|
| `feat`        | Nueva funcionalidad de código                               |
| `fix`         | Corrección de un bug                                        |
| `chore`       | Tareas de mantenimiento (deps, config, tooling)              |
| `docs`        | Documentación técnica (arquitectura, setup, README)          |
| `docs-design` | Documentación de diseño (lore, characters, environment)         |
| `refactor`    | Cambio de código que no agrega feature ni arregla bug         |
| `test`        | Agregar o corregir tests                                     |

Ejemplos:
```
docs-design: add villain motivation to lore
docs: document Colyseus room setup
feat: add player movement sync
fix: prevent duplicate chat messages
chore: update phaser to 3.80
```

## Resumen rápido

- Código → inglés, siempre, con rama `feature/*` y commit `feat:`/`fix:`.
- Doc de diseño → contenido en español, nombre de archivo en inglés, commit
  directo con prefijo `docs-design:`.
- Doc técnico → contenido en español, dentro de la rama de la feature que
  documenta, commit `docs:`.
