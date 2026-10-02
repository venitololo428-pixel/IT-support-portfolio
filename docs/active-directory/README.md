# Active Directory — Laboratorio práctico

Laboratorio construido en Hyper-V con un Domain Controller (Windows Server, AD DS + DNS + DHCP) y múltiples VMs cliente unidas al dominio.

## Temas cubiertos

- Promoción de DC, DNS, DHCP (autorización y scopes)
- Organización de OUs y grupos siguiendo el patrón **AGDLP** (Accounts → Global → Domain Local → Permissions)
- GPOs: herencia, regla LSDOU, Enforced, Computer Configuration vs User Configuration
- Delegación de control
- Troubleshooting real: IP APIPA en el DC, DHCP no autorizado, Enhanced Session Mode bloqueando RDP, ruptura de secure channel causada por Checkpoints de Hyper-V, registros de DHCP huérfanos en AD
- Impresoras en AD: instalación, publicación en el directorio, despliegue vía GPO

## Documento

Ver [`Casos_Estudio_AD_DHCP.pdf`](./Casos_Estudio_AD_DHCP.pdf) (vista previa directa) o [`.docx`](./Casos_Estudio_AD_DHCP.docx) para los casos de estudio detallados en formato Situación → Diagnóstico → Causa raíz → Acción → Resultado (base para respuestas STAR en entrevistas).
