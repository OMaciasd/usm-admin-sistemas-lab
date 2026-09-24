# USM Admin Lab — AGENTS.md

## Objetivo
Construir un laboratorio virtual reproducible, documentado y verificable para la preparación del primer certamen de Administración de Sistemas (USM).

## Estructura
- `docs/` — documentación del laboratorio, estado del entorno, dependencias Cisco, etc.
- `infra/` — definiciones de VMs, scripts de provisionamiento, plantillas de GNS3/Vmware.
- `scripts/` — scripts de automatización (Ansible, Terraform, etc.).
- `tests/` — tests de validación de configuraciones.
- `README.md` — descripción general y puesta en marcha.

## Política de licenciamiento
Solo software de uso autorizado. Ver `docs/cisco-dependency.md` y `docs/lab-status.md`. Está prohibido subir imágenes Cisco, credenciales, certificados privados o secretos al repositorio.

## Política Git
- `main` es la rama por defecto y protegida.
- Prohibido push directo, force push y eliminación de ramas.
- Todo cambio debe realizarse en una rama de trabajo (`feat/...`) y fusionarse mediante Pull Request con revisión y checks.
- El primer commit es un baseline: `chore: 🏗️ init lab repo`.

## Política de estados de implementación
Cada componente debe etiquetarse con uno de los siguientes estados:
- `IMPLEMENTED`: código/script/estructura creado.
- `VERIFIED`: probado en el entorno.
- `PARTIAL`: parcialmente funcional, falta algún aspecto.
- `BLOCKED`: imposibilitado por restricciones de licencia o hardware.

## Política de validación
Nada se da por sentado. Antes de afirmar que una tecnología funciona:
1. Verificar existencia.
2. Verificar compatibilidad.
3. Verificar licencia.
4. Ejecutar en el entorno y registrar resultados.
5. Documentar limitaciones.

## Prohibición de trabajar sobre `main`
Nunca se trabaja directamente sobre `main`. Todos los cambios deben hacerse en ramas `feat/` y fusionarse mediante PR.

## Secretos
Nunca subir credenciales, claves privadas, certificados o secretos al repositorio.