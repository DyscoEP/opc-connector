# Limitaciones y problemas

- Portable de escritorio: cerrar sesión o salir puede detenerlo; no es servicio de Windows.
- Si DA no aparece en el cliente, revisa arquitectura, Core Components, OPCEnum y registro. Abre la aplicación antes del cliente. Registrar para todos requiere UAC y puede solucionar visibilidad del servicio OPCEnum.
- Un endpoint UA accesible no implica confianza de certificados ni permisos de usuario. Revisa interfaz, endpoint anunciado y política del cliente; no se promete compatibilidad con cualquier cliente/firmware.
- Un tipo PLC incorrecto se rechaza cuando puede detectarse. Confirma formato, cantidad de registros, dirección y orden de bytes.
- Un timeout de escritura puede significar que el equipo sí la aplicó. Revisa el valor antes de repetir; no hay reintento automático.
- Una consulta histórica necesita una fecha válida y un criterio de desempate. Tag Puntual exige ID único.
- La calidad inferida o la clasificación 0/1 como Boolean debe revisarse según significado de la señal.
- Al cambiar de cuenta o equipo, vuelve a introducir las credenciales de tus conexiones.
- Logs, alarmas y colas tienen límites. Pausar el visor no pausa adquisición y el historial puede rotar.
- Consulta [drivers y límites](drivers-y-limites.md) antes de asumir soporte de redes o interfaces antiguas.

Al reportar, indica versión/build, Windows, driver, arquitectura COM, modelo/firmware y pasos mínimos. Adjunta solo capturas y datos depurados; nunca claves ni proyectos completos de clientes.
