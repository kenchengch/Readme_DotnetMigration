## Installing tools
```dotnetcli
dotnet tool install --global dotnet-ef
```

```dotnetcli
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet add package Pomelo.EntityFrameworkCore.MySql
```

## Verify installation

Run the following commands to verify that EF Core CLI tools are correctly installed:

  ```dotnetcli
  dotnet ef
  ```

The output from the command identifies the version of the tools in use:

```output
_/\__
---==/    \\
___  ___   |.    \|\
| __|| __|  |  )   \\\
| _| | _|   \_/ |  //|\\
|___||_|       /   \\\/\\

Entity Framework Core .NET Command-line Tools 2.1.3-rtm-32065

<Usage documentation follows, not shown.>
```

## Add migration script MyScriptCreate
```dotnetcli
dotnet ef migrations add MyScriptCreate
```
## Run Migration
```dotnetcli
dotnet ef database update
```
##Generate Script for Production
```dotnetcli
dotnet ef migrations script 0 Migration1 --output Migration1.sql
dotnet ef migrations script Migration1 Migration2 --output Migration2.sql
dotnet ef migrations script Migration2 Migration3 --output Migration3.sql
```dotnetcli
