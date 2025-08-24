Running the Project

Install EF Core Tools (if not already)

Open Package Manager Console:
Tools > NuGet Package Manager > Package Manager Console

Check installation:

Get-Help about_EntityFrameworkCore


If missing, install:

Install-Package Microsoft.EntityFrameworkCore.Tools


Set Startup Project

In Solution Explorer, right-click NZWalks.API → Set as Startup Project.

Set Default Project in PMC

In Package Manager Console, select NZWalks.API (where DbContext lives) as the Default project.

Create Migration

Add-Migration InitialCreate -Context NZWalksDbContext


→ Creates a Migrations folder in NZWalks.API.

Apply Migration

Update-Database -Context NZWalksDbContext


→ Builds the database using appsettings.json connection string.
(Update the connection string if needed.)

Run API & UI Together

Right-click solution → Properties → Set both NZWalks.API and NZWalks.UI as startup projects.
