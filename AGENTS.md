## Objetivo
Construir un laboratorio virtual reproducible, documentado y verificable para la preparación del primer certamen de Administración de Sistemas (USM).

## Estructura
- `docs/` — documentación del laboratorio, estado del entorno y dependencias.
- `infra/` — definiciones de VMs y plantillas de infraestructura.
- `scripts/` — automatización.
- `tests/` — validaciones.
- `README.md` — descripción general y puesta en marcha.

## Contrato para agentes
- Mantener `AGENTS.md` versionado porque contiene el contrato permanente, general y reproducible del proyecto.
- No incluir credenciales, tokens, contraseñas, secretos, claves privadas, certificados privados, endpoints internos, hosts privados, datos personales, rutas personales ni detalles de otros proyectos innecesarios para el laboratorio.

## Seguridad y licenciamiento
- Usar únicamente software e imágenes autorizados; no subir imágenes Cisco ni material de terceros sin autorización.
- Verificar la licencia y la autorización de dependencias e imágenes; registrar dependencias y limitaciones en la documentación permanente.

## Reutilización y cambios no destructivos
- Antes de modificar, inspeccionar los recursos existentes y no duplicar implementación o documentación reutilizable.
- Priorizar la reutilización segura y validar cualquier adaptación antes de aplicarla.
- No realizar cambios destructivos, eliminar archivos ni sobrescribir trabajo no relacionado sin solicitud explícita y revisión previa.

## Higiene documental
- Versionar documentación Markdown solo cuando tenga valor permanente para reproducir, operar, mantener, diagnosticar, preparar el certamen o gestionar decisiones futuras.
- No versionar rutinariamente scratchpads como `PLAN.md`, `TODO.md`, `TASKS.md`, `NOTES.md` y `SCRATCH.md`, ni notas internas, logs, debugging, planes consumidos o artefactos generados sin valor permanente.
- Antes de crear un `.md`, buscar documentación existente y actualizar el documento equivalente; crear uno nuevo solo para una responsabilidad documental distinta.

## Git y Pull Requests
- Trabajar mediante ramas `feat/...`; no hacer push directo a `main`, force push ni eliminar ramas.
- No usar `git add .` indiscriminadamente; antes de agregar archivos revisar `git status`, `git diff --stat` y `git diff --cached --stat`, y agregar solo los archivos pertinentes.
- No crear commits, tags, releases ni Pull Requests sin solicitud explícita.
- Cada cambio debe pasar por Pull Request con revisión y checks antes de fusionarse.
- Usar Conventional Commits con el formato `<type>(<scope>): <description>` y tipos como `feat`, `fix`, `docs`, `test`, `chore` o `refactor`.

## Validación
- Antes de declarar una tecnología como verificada, comprobar existencia, disponibilidad, compatibilidad, licencia, autorización y funcionamiento; ejecutar la validación disponible y documentar resultados, limitaciones y bloqueos.
- Antes de cerrar cambios, ejecutar lint, typecheck, tests o validaciones equivalentes que existan en el repositorio.

## Estados de implementación
Cada componente debe etiquetarse con uno de los siguientes estados:
- `IMPLEMENTED`: código, script o estructura creado.
- `VERIFIED`: probado en el entorno.
- `PARTIAL`: parcialmente funcional; falta completar algún aspecto.
- `BLOCKED`: impedido por restricciones de licencia, hardware o entorno.
