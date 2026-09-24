# USM – Administración de Sistemas Laboratorio

Laboratorio virtual reproducible para la preparación del primer certamen de Administración de Sistemas de la USM.

## Objetivo
Ofrecer un entorno técnico donde aprender y verificar conceptos de redes y administración de sistemas, basándose en Rocky Linux 10, VMware Workstation, GNS3, VLANs, 802.1Q, Router-on-a-Stick, DHCP, dnsmasq, RADIUS, FreeRADIUS, TLS, routing, diseño jerárquico, Collapsed Core, Spine-Leaf, East‑West traffic, QinQ/802.1ad, VXLAN, VTEP, VNI, BGP, EVPN, VRF, multi‑tenancy, Fabric‑Based Networking, troubleshooting y automatización.

## Alcance
El laboratorio cubre teoría y práctica. Se utilizan herramientas de código abierto siempre que sea posible; las dependencias de Cisco se documentan por separado y no se almacenan en el repositorio.

## Estado actual
- Repositorio inicializado (`main` protegido, baseline `chore: 🏗️ init lab repo`).
- Se ha inspeccionado el entorno y se documenta en `docs/lab-status.md`.
- Dependencias Cisco pendientes de licencia (ver `docs/cisco-dependency.md`).

## Próximos pasos
1. Crear la rama `feat/lab-foundation` a partir de `main`.
2. Definir la topología de red (VLANs, Router‑on‑a‑Stick).
3. Provisionar Rocky Linux 10 como servidor DHCP/dnsmasq.
4. Implementar FreeRADIUS con AAA.
5. Configurar BGP y EVPN sobre un spine‑leaf simulado.
6. Añadir scripts de automatización (Ansible).
7. Documentar tests de validación.
8. Publicar el laboratorio una vez verificado.

## Cómo contribuir
1. Crear una rama `feat/...` a partir de `main`.
2. Realizar los cambios.
3. Hacer commit y push.
4. Abrir un Pull Request; esperar aprobación y checks.
5. Tras la aprobación, mergear a `main`.

## Licencia
Ver `AGENTS.md` para la política de licenciamiento del laboratorio. No subir imágenes Cisco, credenciales ni secretos.