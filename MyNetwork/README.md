**Languages:** [English](README.md) · [Español](README.es.md)

# MyNetwork

Contactinet.Web prototype based on ASP.NET Core Razor Pages with ASP.NET Identity user accounts, SQL persistence, and Azure deployment configuration.

Documentation based on local files reviewed on 21 October 2026.

<!-- BEGIN project-context -->

## Historical dates and evidence

**Reference year for this version: 2019.** This uses the most recent source or configuration file with a recoverable historical date; the exact creation date could not be confirmed.

- Most recent datable file: **2019-11-14**, [`MyNetwork/azure-pipelines.yml`](azure-pipelines.yml); preserved modification timestamp.
- First record in the original Git repository containing this code: **2019-11-13**. This may be an import and does not establish when the code was first written.
- Most recently published dependency among those checked: [Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore 3.0.0](https://www.nuget.org/packages/Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore/3.0.0), published on **2019-09-23** (declared version), in [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj).
- Additional reference: target `netcoreapp3.0` in [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj); its [stable release was published on 2019-09-23](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core). This indicates the technology generation; earlier preview releases may have existed.

A dependency's publication places the preserved configuration at or after that version, if the reference is valid. Package updates may be much newer than the project's beginnings. Packages were not restored to verify this.

## Why this is worth exploring

The visible portion is a Razor Pages foundation with Identity and Entity Framework migrations. It is a useful authentication and persistence reference for a prototype; the preserved code does not yet implement a complete contact network.

Code entry points:

- [`Contactinet.Web/Contactinet.Web/Startup.cs`](Contactinet.Web/Contactinet.Web/Startup.cs)
- [`Contactinet.Web/Contactinet.Web/Data`](Contactinet.Web/Contactinet.Web/Data/)
- [`Contactinet.Web/Contactinet.Web/Pages`](Contactinet.Web/Contactinet.Web/Pages/)

<!-- END project-context -->

## Structure and responsibilities

| Path | Responsibility |
| --- | --- |
| `Contactinet.Web/Contactinet.Web/` | Razor Pages application and ASP.NET Core startup. |
| `Contactinet.Web/Contactinet.Web/Data/` | ApplicationDbContext and Identity schema migrations. |
| `Contactinet.Web/Contactinet.Web/Pages/` | Template home, privacy, error pages, and layouts. |
| `Contactinet.Web/Contactinet.Web/Properties/PublishProfiles/` | Deployment profiles and local user files. |
| `azure-pipelines.yml` | Existing pipeline definition. |

## Technologies and requirements

.NET Core 3.0, Entity Framework Core 3, SQL Server/LocalDB, and tools compatible with ASP.NET Core Identity.

Targets read from project files: `netcoreapp3.0`.

## Setup and startup

Prepare DefaultConnection and review Startup before starting the web project. Migrations create Identity tables and should only be applied to an explicitly selected database.

Setup commands, run from this folder after reviewing private configuration:

```text
dotnet restore Contactinet.Web/Contactinet.Web.sln
dotnet build Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj
```

Solutions present: `Contactinet.Web/Contactinet.Web.sln`.

## Configuration and integrations

appsettings.json declares DefaultConnection and AppSettings:dbConnection. .pubxml.user profiles are private and may contain encrypted publish passwords.

## Status of this copy

The visible copy mainly preserves a Razor Pages/Identity scaffold; it does not demonstrate a complete working contact network. Migrations and pipelines were not run.

The review was static: dependencies were not restored, and applications and tests were neither built nor run. The commands above are setup instructions, not validation results. Listed versions describe the preserved code.


## Public copy

Original credentials have been removed or replaced with `REPLACE_WITH_YOUR_VALUE`. Local data, sessions, private certificates, and deployment profiles are omitted. Configure your own services and credentials before running. Building and operation with external services have not been validated.
