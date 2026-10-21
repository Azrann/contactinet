# MyNetwork

Prototipo Contactinet.Web basado en ASP.NET Core Razor Pages con cuentas de usuario ASP.NET Identity, persistencia SQL y configuración de despliegue Azure.

Documentación basada en los archivos locales revisados el 21 de octubre de 2026.

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
