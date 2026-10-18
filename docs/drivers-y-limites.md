# Drivers y límites

| Fuente | Alcance |
|---|---|
| Modbus TCP/RTU | Lectura y escritura de coils/holding registers con permiso por tag; entradas y registros de entrada son lectura. Tipos y órdenes configurables. |
| MySQL / SQL Server | Navegación de tablas, vista de registros e importación con mapeo; Tag Histórico o Tag Puntual. Solo lectura. |
| JSON/REST | Lectura HTTP/HTTPS con rutas de objeto, valor, calidad y fecha. No escribe al servicio origen. |
| OPC DA local | Servidores locales de 32/64 bits, exploración, lectura y escritura según derechos. Únicamente máquina local; remoto mediante UA. |
| OPC UA / túnel | Suscripciones, calidad/fecha, namespace y derechos de origen, certificados y prevención de ciclos. Descubrimiento de servidores compatibles en la red local. |
| ICMP | Disponibilidad IPv4, latencia, pérdida, TTL y estado; lectura. |
| SNMP | GET/Walk v1/v2c/v3, SHA/SHA256 y AES-128 según configuración. Walk limitado; sin SET ni traps. |
| Siemens S7 TCP | Acceso a DB/M/I/Q y formatos compatibles. Entradas solo lectura; DB/M/Q escribibles con permiso. No PROFINET IO ni PROFIBUS/MPI directo. |
| ControlLogix/CompactLogix | EtherNet/IP con ruta/slot, símbolos y miembros escalares. Exploración según controlador y acceso externo. |
| Micro800 | EtherNet/IP directo en modelos compatibles, sin ruta backplane. Símbolos compatibles según firmware. |
| SLC/MicroLogix / PLC-5 | Acceso mediante EtherNet/IP, archivos N/B/F/L/ST y bits compatibles. Sin CSPv4 TCP-2222. |
| DH+ vía gateway | Ruta mediante módulo/gateway DHRIO compatible, canal y nodos. Requiere hardware. No Data Highway original ni DH-485. |
| DF1 Serial | SLC/MicroLogix Full Duplex de 8 bits, CRC/BCC, archivos N/B/F/L y bits. Sin PLC-5 DF1, Half Duplex ni STRING DF1. |
| Serial personalizado | Configuración serial disponible; la adquisición requiere un protocolo específico y no forma parte de las fuentes de lectura genéricas. |
| Tags calculados | Escala, factor y ecuaciones con funciones y referencias. Solo lectura, con intervalo y antigüedad. |

Arrays Rockwell se crean/importan como elementos escalares; los UDT requieren miembros escalares explícitos. No se implementan temporizadores, contadores ni I/O legadas por dirección. L5X importa declaraciones compatibles, no proyectos ACD ni programas al PLC.

Alarmas: reglas locales y salida OPC A&E 1.10 / UA A&C. No importa alarmas A&E externas ni ofrece historian, ramas históricas, shelving o confirmación completa. La retención es limitada.

Disponible para Windows 10/11 x64. Las funciones de cada equipo dependen de su modelo, firmware, configuración e interfaz.
