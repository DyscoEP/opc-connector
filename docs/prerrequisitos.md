# Prerrequisitos

- Windows 10/11 x64. Extrae todo el paquete para ejecutar la aplicación.
- OPC UA, cálculos y REST usan componentes incluidos. El cliente remoto debe confiar en el certificado y cumplir la política configurada.
- OPC DA/A&E y fuente OPC DA local: .NET Framework 4.8 y OPC Core Components x64. Para clientes/servidores fuente de 32 bits, también Core Components x86. Obtén instaladores y condiciones en [OPC Foundation](https://opcfoundation.org/developer-tools/samples-and-tools-classic/core-components/).
- Abre OPC Connector antes de conectar clientes DA. El registro por usuario y OPCEnum pueden requerir registrar para todos con UAC.
- SQL Server: controlador ODBC correspondiente, por ejemplo [Microsoft ODBC Driver 18](https://learn.microsoft.com/sql/connect/odbc/download-odbc-driver-for-sql-server). Revisa cifrado, certificado y autenticación Windows/SQL.
- MySQL usa el cliente incluido; requiere servidor accesible y permisos de consulta.
- Modbus RTU y DF1: adaptador serial y controlador de Windows apropiados. No sustituyen interfaces DH+/DH-485/PROFIBUS.
- Siemens y Rockwell requieren acceso externo habilitado por el responsable del PLC, direcciones compatibles y permisos de lectura/escritura. El programa no configura ni descarga programas al PLC.

Esta edición se ejecuta como aplicación de escritorio y debe permanecer abierta para adquirir y publicar datos. Consulta [drivers y límites](drivers-y-limites.md).
