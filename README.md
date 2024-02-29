# watchWorld
A Sample N-layered .NET Core Project Demonstrating Clean Architecture and the Generic Repository Pattern

## packages

### ApplicationCore
- Ardalis.Specification

### InfraStructure
- Microsoft.EntityFrameWorkCore
- Microsoft.EntityFrameWorkCore.Design
- Microsoft.EntityFrameWorkCore.Tools
- Npgsql.EntityFrameWorkCore.PostgreSQL

### Web
Microsoft.EntityFrameworkCore.Design

### UnitTest
...

## Migrations

Before running the following commands, ensure that "Web" is set as the startup project. Run the following commands in the "Infrastructure" project.

```
Add-Migration InitialCreate -Context WatchWorldContext -OutputDir Data/Migrations
Update-Database -Context WatchWorldContext

Add-Migration InitialIdentity -Context AppIdentityDbContext -OutputDir Identity/Migrations
Update-Database -Context AppIdentityDbContext
```