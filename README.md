# WorkIS

**Versión:** `v0.1.0`

WorkIS es una skill para gestionar el ciclo documental de tarjetas de cambio en uno o varios sistemas: crea ATF iterativos, estima trabajo frontend y redacta comentarios funcionales para Trello.

## Qué hace

| Modo | Resultado |
|---|---|
| ATF | Crea y versiona un Análisis Técnico-Funcional en Markdown. |
| Estimación frontend | Genera un checklist con horas, listo para pegar en Trello. |
| Comentario de rama | Documenta en Trello lo incorporado por una rama. |
| Comentario de commit | Documenta en Trello un commit específico. |
| Comentario desde ATF | Contrasta AF/ATF aprobados con lo implementado. |
| Comentario de sesión | Documenta decisiones y validaciones conversadas, contrastadas con los cambios reales. |

Los comentarios de Trello son funcionales y no técnicos. Usan una plantilla fija con contexto, cambio, uso, impacto, validaciones, referencias y consideraciones de publicación.

## Comandos de WorkIS

En Codex, invocá la skill con `$workis` seguido del modo y los datos disponibles.

```text
$workis atf para ART, tarjeta SXqqL1vS
$workis estimar para ART usando el ATF de SXqqL1vS
$workis comentario-rama para ART, tarjeta ABC-123
$workis comentario-commit para ART, commit a1b2c3d
$workis comentario-atf para ART, tarjeta ABC-123
$workis comentario-sesion para ART, tarjeta ABC-123
```

También se puede invocar en lenguaje natural:

```text
Usá WorkIS para crear el ATF de la tarjeta SXqqL1vS para ART.
Usá WorkIS para preparar el comentario Trello de esta rama.
```

Si no se indica el modo, WorkIS pregunta si se necesita un ATF, una estimación o un comentario. Para comentarios, pide elegir una única fuente: rama, commit, ATF aprobado o sesión.

## Primera configuración de un proyecto

La primera vez que uses un proyecto, WorkIS pedirá:

1. Nombre del sistema/proyecto.
2. Ruta del repositorio.
3. Rutas de frontend y backend, si corresponden.
4. Ubicación habitual de AF, ATF y recursos.
5. Rama base habitual.
6. Carpeta para guardar ATF.
7. Carpeta para guardar copias de comentarios, si las solicitás.

El perfil se guarda localmente fuera del repositorio de WorkIS:

```text
Windows: %USERPROFILE%\.workis\projects.local.json
Otros sistemas: ~/.workis/projects.local.json
```

Así las rutas personales no se suben a Git.

## Comportamiento por modo

### ATF

- Requiere un AF aprobado como fuente principal. Si no está disponible, puede hacer un borrador con el pendiente marcado.
- Usa la guía del proyecto, recursos, código y la [plantilla ATF](templates/plantilla-atf.md).
- No elimina secciones de la plantilla: usa `No aplica` con justificación cuando corresponda.
- Crea versiones independientes y nunca sobrescribe una anterior:

```text
Sistema_IDTarjeta_ATF_v0.1.md
Sistema_IDTarjeta_ATF_v0.2.md
Sistema_IDTarjeta_ATF_V1.md
```

- Solo genera `V1` después de una aprobación explícita.

### Estimación frontend

Solo considera trabajo de frontend respaldado por un ATF aprobado. La respuesta contiene exclusivamente el checklist para Trello.

Estas tareas aparecen siempre:

```text
Análisis Técnico Funcional de la Incidencia +2hs
Completado de Tarjeta +30min
PR +20min
```

### Comentarios de Trello

WorkIS analiza en solo lectura y no modifica el repositorio. No inventa validaciones, impactos, enlaces ni decisiones. Si pedís una copia local del comentario, propone crear:

```text
Sistema_IDTarjeta_CambioImplementado.md
```

Trello continúa siendo el registro principal.

## Instalación en Codex

### Opción A: clonar desde Git

Reemplazá `URL_DEL_REPOSITORIO` por la URL de WorkIS:

```powershell
git clone URL_DEL_REPOSITORIO "$env:USERPROFILE\.codex\skills\workis"
```

Abrí un chat nuevo de Codex y usá cualquiera de los comandos de la sección anterior.

### Opción B: enlazar una copia local durante el desarrollo

Esta opción permite que los cambios en el repositorio se reflejen directamente en Codex:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills"
New-Item -ItemType Junction `
  -Path "$env:USERPROFILE\.codex\skills\workis" `
  -Target "C:\Users\User\Desktop\WorkIS"
```

Si ya existe `workis` en esa ubicación, no ejecutes el segundo comando: primero eliminá o renombrá el enlace o copia existente de forma consciente.

## Instalación en Claude Code

Cloná o enlazá la misma carpeta dentro del directorio de skills de Claude Code:

```powershell
git clone URL_DEL_REPOSITORIO "$env:USERPROFILE\.claude\skills\workis"
```

Después, en un chat de Claude Code, invocala así:

```text
/workis atf para ART, tarjeta SXqqL1vS
/workis comentario-rama para ART, tarjeta ABC-123
```

## Actualizar WorkIS

Si instalaste WorkIS mediante `git clone`:

```powershell
git -C "$env:USERPROFILE\.codex\skills\workis" pull
```

Si usás un enlace local, no necesitás actualizar: Codex utiliza los archivos del repositorio enlazado.

## Versionar y publicar el repositorio

La rama principal es `main`. Para crear el primer commit y asociar un remoto:

```powershell
Set-Location "C:\Users\User\Desktop\WorkIS"
git branch -M main
git add .
git commit -m "feat: create WorkIS v0.1.0"
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

Reemplazá `URL_DEL_REPOSITORIO` por la URL HTTPS o SSH del repositorio remoto que crees.

## Estructura

```text
WorkIS/
├── SKILL.md
├── README.md
├── references/
│   ├── atf.md
│   ├── comentarios-trello.md
│   └── estimacion-frontend.md
└── templates/
    └── plantilla-atf.md
```
