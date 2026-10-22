**Languages:** [English](README.md) · [Español](README.es.md)

# contactinet

Contactinet web application.

<!-- BEGIN project-context -->

## Historical dates and evidence

**Reference year for this version: 2019.** This uses the most recent source or configuration file with a recoverable historical date; the exact creation date could not be confirmed.

- Most recent datable file: **2019-11-14**, [`MyNetwork/azure-pipelines.yml`](MyNetwork/azure-pipelines.yml); preserved modification timestamp.
- First record in the original Git repository containing this code: **2019-11-13**. This may be an import and does not establish when the code was first written.
- Most recently published dependency among those checked: [Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore 3.0.0](https://www.nuget.org/packages/Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore/3.0.0), published on **2019-09-23** (declared version), in [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj).
- Additional reference: target `netcoreapp3.0` in [`MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj`](MyNetwork/Contactinet.Web/Contactinet.Web/Contactinet.Web.csproj); its [stable release was published on 2019-09-23](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core). This indicates the technology generation; earlier preview releases may have existed.

A dependency's publication places the preserved configuration at or after that version, if the reference is valid. Package updates may be much newer than the project's beginnings. Packages were not restored to verify this.

## Why this is worth exploring

The visible portion is a Razor Pages foundation with Identity and Entity Framework migrations. It is a useful authentication and persistence reference for a prototype; the preserved code does not yet implement a complete contact network.

Code entry points:

- [`Contactinet.Web/Contactinet.Web/Startup.cs`](MyNetwork/Contactinet.Web/Contactinet.Web/Startup.cs)
- [`Contactinet.Web/Contactinet.Web/Data`](MyNetwork/Contactinet.Web/Contactinet.Web/Data/)
- [`Contactinet.Web/Contactinet.Web/Pages`](MyNetwork/Contactinet.Web/Contactinet.Web/Pages/)

<!-- END project-context -->

## Contents

| Directory | Function |
| --- | --- |
| [`MyNetwork/`](MyNetwork/) | Contactinet.Web prototype based on ASP.NET Core Razor Pages with ASP.NET Identity user accounts, SQL persistence, and Azure deployment configuration. |



## Requirements and setup

.NET Core 3.0, ASP.NET Core MVC, Identity, and Entity Framework.

This is a historical copy. Consult each component's project files and README for versions and dependencies. Restore NuGet/npm from the appropriate folder; internal libraries may need rebuilding. Prepare databases and external services using your own accounts.

Preserved solutions:

- `MyNetwork/Contactinet.Web/Contactinet.Web.sln`

## Configuration and security

Original secrets have been removed or replaced with `REPLACE_WITH_YOUR_VALUE`. Search for this marker before running and provide values through local configuration or environment variables. Sessions, private keys, signing certificates, databases, logs, deployment profiles, and binary packages are not published. The `.gitignore` protects these local files.

A fresh history is published: old commits remain only in the original local copy. Example values cannot connect to the original services.

## Validation status

A static review and secret scan were performed before publication. Applications, trading operations, deployments, and tests contacting external services were not run. Building with current tools is not guaranteed. Some projects need historical dependencies and assets that are not included.

## Licenses and provenance

Third-party licenses and attributions present in the code are retained. No blanket license is added to components that lacked one. This import preserves local sources and does not claim to be a current version of the original project.
