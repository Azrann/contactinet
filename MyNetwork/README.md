# MyNetwork

Prototipo Contactinet.Web basado en ASP.NET Core Razor Pages con cuentas de usuario ASP.NET Identity, persistencia SQL y configuración de despliegue Azure.

Documentación basada en los archivos locales revisados el 21 de octubre de 2026.

<!-- BEGIN project-context -->

## Antigüedad y evidencia

**Año de referencia de esta versión: 2019.** Se toma el archivo de código o configuración más reciente con una fecha histórica recuperable; no se ha podido confirmar la fecha exacta de creación.

- Archivo más reciente datable: **2019-11-14**, [`MyNetwork/azure-pipelines.yml`](azure-pipelines.yml); fecha de modificación conservada.
- Primer registro del repositorio Git original que contiene este código: **2019-11-13**. Puede corresponder a una importación; no prueba cuándo se escribió por primera vez.
- Dependencia fechada más reciente entre las comprobadas: [Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore 3.0.0](https://www.nuget.org/packages/Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore/3.0.0), publicada el **2019-09-23** (versión declarada), en [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj).
- Referencia adicional: destino `netcoreapp3.0` en [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj); su [versión estable se publicó el 2019-09-23](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core). Es una pista de generación tecnológica; pudieron existir versiones preliminares anteriores.

La publicación de una dependencia sitúa la configuración conservada a partir de esa versión, si la referencia es válida. Una actualización de paquetes puede ser mucho más reciente que el inicio del proyecto. No se restauraron paquetes para comprobarlo.

## Por qué merece la pena mirarlo

La parte visible es una base Razor Pages con Identity y migraciones de Entity Framework. Tiene interés como referencia de autenticación y persistencia de un prototipo; el código conservado todavía no desarrolla una red de contactos completa.

Puntos de entrada al código:

- [`Contactinet.Web/Contactinet.Web/Startup.cs`](Contactinet.Web/Contactinet.Web/Startup.cs)
- [`Contactinet.Web/Contactinet.Web/Data`](Contactinet.Web/Contactinet.Web/Data/)
- [`Contactinet.Web/Contactinet.Web/Pages`](Contactinet.Web/Contactinet.Web/Pages/)

<!-- END project-context -->

## Estructura y responsabilidades

| Ruta | Responsabilidad |
| --- | --- |
| `Contactinet.Web/Contactinet.Web/` | Aplicación Razor Pages y arranque ASP.NET Core. |
| `Contactinet.Web/Contactinet.Web/Data/` | ApplicationDbContext y migraciones del esquema Identity. |
| `Contactinet.Web/Contactinet.Web/Pages/` | Inicio, privacidad, errores y layouts de la plantilla. |
| `Contactinet.Web/Contactinet.Web/Properties/PublishProfiles/` | Perfiles de despliegue y archivos locales del usuario. |
| `azure-pipelines.yml` | Definición de pipeline existente. |

## Tecnologías y requisitos

.NET Core 3.0, Entity Framework Core 3, SQL Server/LocalDB y herramientas compatibles con ASP.NET Core Identity.

Destinos leídos de los proyectos: `netcoreapp3.0`.

## Preparación y arranque

Preparar DefaultConnection y revisar Startup antes de iniciar el proyecto web. Las migraciones crean tablas de Identity y solo deben aplicarse a una base elegida de forma explícita.

Comandos de preparación, desde esta carpeta, después de revisar la configuración privada:

```text
dotnet restore Contactinet.Web/Contactinet.Web.sln
dotnet build Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj
```

Soluciones presentes: `Contactinet.Web/Contactinet.Web.sln`.

## Configuración e integraciones

appsettings.json declara DefaultConnection y AppSettings:dbConnection. Los perfiles .pubxml.user son privados y pueden contener contraseñas de publicación cifradas.

## Estado de esta copia

La copia visible conserva principalmente el esqueleto de Razor Pages/Identity; no demuestra una red de contactos funcional completa. No se ejecutaron migraciones ni pipelines.

La revisión fue estática: no se restauraron dependencias, no se compiló ni se ejecutaron aplicaciones o pruebas. Los comandos anteriores son instrucciones de preparación, no resultados de validación. Las versiones indicadas son las del código conservado.


## Copia pública

Las credenciales originales se han retirado o sustituido por `REPLACE_WITH_YOUR_VALUE`. Los datos locales, sesiones, certificados privados y perfiles de despliegue se omiten. Configurar servicios y credenciales propios antes de ejecutar. La compilación y el funcionamiento con servicios externos no se han validado.
