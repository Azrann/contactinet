**Languages:** [English](README.md) · [Español](README.es.md)

# contactinet

Aplicación web Contactinet.

<!-- BEGIN project-context -->

## Antigüedad y evidencia

**Año de referencia de esta versión: 2019.** Se toma el archivo de código o configuración más reciente con una fecha histórica recuperable; no se ha podido confirmar la fecha exacta de creación.

- Archivo más reciente datable: **2019-11-14**, [`MyNetwork/azure-pipelines.yml`](MyNetwork/azure-pipelines.yml); fecha de modificación conservada.
- Primer registro del repositorio Git original que contiene este código: **2019-11-13**. Puede corresponder a una importación; no prueba cuándo se escribió por primera vez.
- Dependencia fechada más reciente entre las comprobadas: [Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore 3.0.0](https://www.nuget.org/packages/Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore/3.0.0), publicada el **2019-09-23** (versión declarada), en [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj).
- Referencia adicional: destino `netcoreapp3.0` en [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj); su [versión estable se publicó el 2019-09-23](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core). Es una pista de generación tecnológica; pudieron existir versiones preliminares anteriores.

La publicación de una dependencia sitúa la configuración conservada a partir de esa versión, si la referencia es válida. Una actualización de paquetes puede ser mucho más reciente que el inicio del proyecto. No se restauraron paquetes para comprobarlo.

## Por qué merece la pena mirarlo

La parte visible es una base Razor Pages con Identity y migraciones de Entity Framework. Tiene interés como referencia de autenticación y persistencia de un prototipo; el código conservado todavía no desarrolla una red de contactos completa.

Puntos de entrada al código:

- [`Contactinet.Web/Contactinet.Web/Startup.cs`](MyNetwork/Contactinet.Web/Contactinet.Web/Startup.cs)
- [`Contactinet.Web/Contactinet.Web/Data`](MyNetwork/Contactinet.Web/Contactinet.Web/Data/)
- [`Contactinet.Web/Contactinet.Web/Pages`](MyNetwork/Contactinet.Web/Contactinet.Web/Pages/)

<!-- END project-context -->

## Contenido

| Directorio | Función |
| --- | --- |
| [`MyNetwork/`](MyNetwork/) | Prototipo Contactinet.Web basado en ASP.NET Core Razor Pages con cuentas de usuario ASP.NET Identity, persistencia SQL y configuración de despliegue Azure. |



## Requisitos y preparación

.NET Core 3.0, ASP.NET Core MVC, Identity y Entity Framework.

Esta es una copia histórica. Consultar los archivos de proyecto y los README de cada componente para sus versiones y dependencias. Restaurar NuGet/npm desde la carpeta correspondiente; las bibliotecas internas pueden necesitar reconstrucción. Preparar las bases de datos y los servicios externos con cuentas propias.

Soluciones conservadas:

- `MyNetwork/Contactinet.Web/Contactinet.Web.sln`

## Configuración y seguridad

Los secretos originales se han eliminado o sustituido por `REPLACE_WITH_YOUR_VALUE`. Buscar este marcador antes de ejecutar y aportar los valores mediante configuración local o variables de entorno. Las sesiones, claves privadas, certificados de firma, bases de datos, registros, perfiles de despliegue y paquetes binarios no se publican. El `.gitignore` protege estos archivos locales.

Se publica un historial nuevo: los commits antiguos permanecen únicamente en la copia local original. Los valores de ejemplo no permiten conectarse a los servicios originales.

## Estado de validación

Se realizó una revisión estática y un escaneo de secretos antes de publicar. No se ejecutaron aplicaciones, operaciones de trading, despliegues ni pruebas que contacten servicios externos. No se garantiza la compilación con herramientas actuales. Algunos proyectos necesitan dependencias históricas y activos que no están incluidos.

## Licencias y procedencia

Se conservan las licencias y atribuciones de terceros presentes en el código. No se añade una licencia global a los componentes que no la tenían. Esta importación conserva fuentes locales y no afirma ser una versión actual del proyecto original.
