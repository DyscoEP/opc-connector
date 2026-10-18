# Guía de uso

## Conexión y tags

Crea una conexión, selecciona la fuente, escribe sus parámetros y pulsa Guardar conexión. En SQL selecciona la tabla cargada desde el servidor; el botón de recarga utiliza los parámetros actuales. La contraseña se puede mostrar u ocultar.

Selecciona la carpeta Tags para ver el explorador. Desde allí importa símbolos/registros o crea tags y lotes cuando el driver lo permite. Las carpetas se administran desde el menú contextual. Elegir un tag en el árbol abre sus propiedades a la derecha; las propiedades comunes permiten edición masiva mediante selección explícita.

## MySQL y SQL Server

Mapea columnas de identificador, valor, calidad y fecha. Tag Histórico toma el último registro por identificador y fecha; Tag Puntual consulta un ID único. Revisa el tipo inferido por cada valor y corrígelo si la semántica de la señal lo requiere. Los empates temporales deben resolverse en la fuente. Son conexiones de lectura.

## Formatos y escritura

El formato de origen determina cómo se interpretan bytes; el tipo OPC determina su publicación. Float32 Modbus utiliza dos registros; Float64 utiliza cuatro. Configura orden de bytes/palabras y dirección correcta.

Los tags nuevos son de lectura. Habilita Lectura y escritura solo en fuentes compatibles. En Tags del servidor, clic derecho > Escribir permite enviar un valor del tipo configurado. Se confirma con el equipo y se relee; no se reintentan escrituras inciertas automáticamente.

## Publicación

Configura DA/A&E, UA, REST y opciones de operación en Configuración del servidor. UA permite interfaces, endpoints, anonimato o usuario y certificados/políticas compatibles. REST es opcional y solo expone lecturas del catálogo adquirido. Iniciar general pone en marcha adquisición y publicación; elegir vistas no altera el estado.

## Cálculos y alarmas

El arquitecto crea tags de escala, factor o ecuación a partir de tags existentes, con intervalo y control de antigüedad. Se validan dependencias y ciclos. Las alarmas locales aplican reglas de valor, estado o calidad. Consulta las opciones de reconocimiento y publicación en [cobertura por fuente](drivers-y-limites.md).

## Guardado y operación

Guarda proyectos .opc.json. Las credenciales se asocian a tu cuenta de Windows; al cambiar de equipo o cuenta debes introducirlas de nuevo. El visor tiene retención limitada y el diario rota. Minimizar mantiene la aplicación en bandeja; Salir detiene los servicios.

[Puesta en marcha](puesta-en-marcha.md) · [Límites](drivers-y-limites.md)
