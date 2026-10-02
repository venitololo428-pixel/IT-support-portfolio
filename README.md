# Gabriel Díaz — Portafolio de IT Support

Panamá, Panamá · Bilingüe (español/inglés) · [venitololo428@gmail.com](mailto:venitololo428@gmail.com)

Profesional en transición hacia roles de **IT Support / Help Desk**, con más de 3 años de experiencia en entornos de BPO y corporativos (soporte técnico, operaciones de back-office, administración de beneficios en EE.UU.). Este repositorio documenta un proceso de preparación técnica hands-on: un laboratorio propio de Active Directory en Hyper-V, práctica de mesa de ayuda en Jira Service Management, y herramientas de soporte remoto — construido y resuelto de forma independiente, no copiado de un curso.

## Habilidades técnicas

| Área | Detalle |
|---|---|
| **Sistemas operativos** | Windows (uso avanzado, administración de Windows Server), conceptos de macOS (equivalencias y soporte multiplataforma) |
| **Active Directory** | Instalación y promoción de Domain Controllers, DNS, DHCP, OUs, grupos con patrón AGDLP, GPOs (herencia LSDOU, Enforced, Computer vs User Configuration), delegación de control, impresoras publicadas y desplegadas vía GPO |
| **Redes** | TCP/IP, subnetting, DNS (zonas, forwarders, registros SRV), DHCP (scopes, autorización, APIPA), direccionamiento privado (RFC 1918) |
| **Mesa de ayuda / Ticketing** | Jira Service Management: request types, colas con JQL, SLAs, reportes, ciclo de vida completo de tickets (resuelto, duplicado, escalado, rechazado) |
| **Soporte remoto** | RDP (dominio/red local), AnyDesk (acceso por internet con autorización explícita) |
| **Virtualización** | Hyper-V: switches virtuales (External, Internal, Private), Enhanced Session Mode, snapshots/checkpoints |
| **Diagnóstico y troubleshooting** | Metodología sistemática: reproducir, aislar causa raíz, corregir, documentar — aplicada en todos los casos de estudio de este repositorio |
| **Herramientas de oficina** | Microsoft 365 (Word, Excel con fórmulas y formato condicional), documentación técnica |

## Contenido del repositorio

| Carpeta | Descripción |
|---|---|
| [`docs/active-directory`](./docs/active-directory) | Laboratorio de AD/DNS/DHCP sobre Hyper-V: casos de estudio reales de troubleshooting (dominios, OUs, grupos AGDLP, GPOs, delegación de control, impresoras) |
| [`docs/jira`](./docs/jira) | Práctica de Jira Service Management: colas, JQL, SLAs, reportes y resolución simulada de tickets |
| [`docs/remote-access`](./docs/remote-access) | Comparativa práctica RDP vs AnyDesk |
| [`docs/macos-vs-windows`](./docs/macos-vs-windows) | Tabla de equivalencias Windows ↔ macOS para soporte multiplataforma |
| [`docs/Portafolio_IT_Support.pdf`](./docs/Portafolio_IT_Support.pdf) | Documento consolidado con las tres secciones principales (AD, Jira, Remote Access Tools) |

## Casos de estudio destacados

Troubleshooting real documentado durante la construcción del laboratorio (detalle completo en [`docs/active-directory`](./docs/active-directory)):

- **Ruptura de secure channel por Checkpoints de Hyper-V** — diagnóstico de fallo de confianza entre dominio y cliente, causa raíz identificada en el uso de snapshots sobre VMs de infraestructura, corregido deshabilitando checkpoints en los servidores
- **DC con IP dinámica (APIPA)** — diagnóstico vía `ipconfig`/`nslookup`, corregido asignando IP estática con DNS autorreferenciado
- **DHCP no autorizado / sin scope activo** — resuelto vía autorización en AD y creación de scope
- **Registro huérfano de servidor DHCP en AD** — diagnosticado con `Get-DhcpServerInDC`, bloqueando nueva autorización
- **Enhanced Session Mode bloqueando acceso remoto** — diferenciado de un problema real de permisos RDP, resuelto vía Group Policy (AGDLP) para RDP delegado por dominio

## Educación y certificaciones

- Google IT Support Professional Certificate (Coursera) — en curso
- Licenciatura en Ingeniería en Sistemas — en curso

## Experiencia profesional previa

- **Alorica** — Soporte técnico Tier 1 (cuenta Best Buy)
- **Foundever** — Operaciones de datos y administración de beneficios, uso de sistemas de ticketing
- **First Enroll** — Accounts Payable Specialist, con cobertura informal de soporte IT interno
