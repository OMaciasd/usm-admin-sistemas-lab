# Laboratorio – Estado del Entorno

## Sistema Operativo
- **Distribución:** Rocky Linux 10 (basado en esta máquina: WSL2 con kernel 6.18.33.2-microsoft-standard)
- **Arquitectura:** x86_64
- **Hardware:** AMD Ryzen 7 7730U con Radeon Graphics, 16 núcleos CPU, 31 GiB de RAM.

## Recursos del Host
- **CPU:** 16 hilos activos (0‑15).
- **Memoria:** 31 GiB total, 8.7 GiB usados, 1.3 GiB de cache, 22 GiB disponibles.
- **Discos:** 
  - `sda` 356.9 M (probablemente USB o temporal)
  - `sdb` 159.4 M
  - `sdc` 8 G
  - `sdd` 1 T

## Virtualización / Hypervisor
- **VMware Workstation:** **No detectado** (`vmrun` no encontrado).
- **GNS3:** **No detectado** (`gns3` no encontrado).
- **Docker:** **Sí** (`docker` disponible).
- **KVM/libvirt:** No hay `/dev/kvm` en este entorno (WSL2).
- **Ansible:** No instalado (`ansible` no encontrado).
- **FRRouting (frr):** No instalado.
- **Python 3.12.3** está disponible.

## Contenedores / Máquinas Virtuales existentes
- Ninguna VM definida en Vmware ni imagen GNS3 en este momento.
- No hay contenedores Docker corriendo (se puede iniciar).

## Hallazgos importantes
1. **No hay hipervisor local** (VMware Workstation) → las VMs de Rocky Linux 10 deberán crearse o bien usarse instancias Docker/WSL2 para pruebas básicas.
2. **No hay GNS3** → cualquier topología de routers/switches deberá construirse con herramientas de línea de comand (Docker, FRRouting, Ansible) o solicitar entorno con GNS3 si disponible.
3. **Herramientas de red:** dnsmasq, FreeRADIUS, BGP, EVPN, VXLAN, VTEP, QinQ, etc., están disponibles para instalarse mediante paquetes `dnf`.
4. **Licencias Cisco:** No hay imágenes Cisco ni licencias; todo el trabajo de Cisco se documentará en `docs/cisco-dependency.md` y se realizará con alternativas open‑source (FRRouting) o quedará `BLOCKED` hasta disponer de una licencia autorizada.

## Próximos pasos de inspección
- Instalar `dnf install -y dnsmasq free-radius frr ansible qemu-kvm` (solo si el hipervisor lo permite) y registrar resultados.
- Definir la topología de laboratorio (VLANs, Router‑on‑a‑Stick, Spine‑Leaf, etc.).
- Crear la rama `feat/lab-foundation` y comenzar el provisionamiento.

--- 

*Este documento se generó automaticamente el $(date +%Y-%m-%d) y forma parte del repositorio `usm-admin-sistemas-lab`.*