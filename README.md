# 🛡️ Laboratorio Seguro de Ciberseguridad

> Configuración y hardening de una máquina virtual de prácticas para el curso de Ciberseguridad.

![Status](https://img.shields.io/badge/status-completado-brightgreen)
![OS](https://img.shields.io/badge/OS-Debian%2013%20Trixie-red)
![Platform](https://img.shields.io/badge/platform-VirtualBox-blue)

---

## 📋 Descripción

Este repositorio contiene el **reporte técnico** de configuración de mi primer laboratorio seguro de ciberseguridad: una máquina virtual (Debian GNU/Linux) creada en Oracle VirtualBox, aislada de mi red doméstica y endurecida (*hardened*) siguiendo buenas prácticas básicas de seguridad.

El objetivo del laboratorio es contar con un entorno controlado y seguro para futuras prácticas del curso (herramientas de pentesting, análisis de malware, etc.) sin poner en riesgo mi máquina real ni mi red local.

---

## 📄 Reporte

📥 **[Ver el reporte completo (PDF)](./Reporte_Lab_Ciberseguridad.pdf)**

El documento incluye evidencia y explicación de cada paso:

| # | Sección | Contenido |
|---|---------|-----------|
| 1️⃣ | **Red Aislada** | Configuración del adaptador de red en modo **NAT** |
| 2️⃣ | **Gestión de Usuarios** | Separación entre usuario administrador (`root`) y usuario estándar (`emiliano`) |
| 3️⃣ | **Actualización del Sistema** | Ejecución de `apt-get update` y `apt-get upgrade` |
| 4️⃣ | **Permisos de Archivos** | Creación de archivo y análisis de permisos con `ls -l` |
| 5️⃣ | **Snapshot** | Punto de restauración `Clean Install - Hardening applied` |

---

## 🧰 Stack utilizado

- **Hipervisor:** Oracle VirtualBox
- **Sistema Operativo (VM):** Debian GNU/Linux 13 (Trixie)
- **Modo de red:** NAT (aislado del host y de la red local)

---

## 🔐 Principios de seguridad aplicados

- ✅ **Aislamiento de red** — la VM no es visible desde la red local ni desde internet
- ✅ **Principio de menor privilegio** — trabajo diario con usuario estándar, no con root
- ✅ **Sistema parcheado** — actualizaciones de seguridad al día
- ✅ **Control de permisos** — gestión explícita de lectura/escritura por archivo
- ✅ **Punto de recuperación** — snapshot para revertir cambios ante cualquier incidente

---

## 👤 Autor

Proyecto realizado como parte del curso de Ciberseguridad — Checkpoint: *Mi primer laboratorio seguro*.
