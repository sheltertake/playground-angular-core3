# playground-angular-core3

ng new SportsStore 
    --directory SportsStore/ClientApp 
    --routing true 
    --style css
    --skip-tests true 
    --skip-git true

ng new SportsStore --directory SportsStore/ClientApp --routing true --style css --skip-tests true --skip-git true

ng s 

---

# Server App

mkdir ServerApp
cd ServerApp
dotnet new globaljson --sdk-version 3.0.100

dotnet new mvc --language C# --auth None
dotnet run

# Certificates

dotnet dev-certs https –-clean
dotnet dev-certs https --trust

# Spa service
dotnet add package Microsoft.AspNetCore.SpaServices.Extensions --version 3.0.0

proxy or managed

# Efcore

dotnet tool uninstall --global dotnet-ef
dotnet tool install --global dotnet-ef --version 3.0.0

dotnet add package Microsoft.EntityFrameworkCore.Design --version 3.0.0
dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 3.0.0

dotnet ef migrations add Initial

dotnet ef database drop --force

# Swashbukle + Json
dotnet add package Swashbuckle.AspNetCore --version 5.0.0-rc2
dotnet add package Microsoft.AspNetCore.Mvc.NewtonsoftJson --version 3.0.0

dotnet ef migrations add ChangeDeleteBehavior

dotnet ef database drop --force
dotnet watch run

# Angular router + mvc fallback + angular components

# Manage client libraries in dotnet web api
dotnet tool install -g Microsoft.Web.LibraryManager.Cli
libman install font-awesome@5.9.0 -p cdnjs -d wwwroot/lib/font-awesome

# Store module -> pagination + rating + fontawasome

# Session
dotnet add package Microsoft.Extensions.Caching.SqlServer --version 3.0.0
dotnet tool uninstall --global dotnet-sql-cache
dotnet tool install --global dotnet-sql-cache --version 3.0.0

dotnet sql-cache create "Server=(localdb)\MSSQLLocalDB;Database=MyEssentialApp" "dbo" "SessionData"

dotnet ef migrations add Orders

# Resetting database

dotnet ef database drop --force
dotnet ef database update
dotnet sql-cache create "Server=(localdb)\MSSQLLocalDB;Database=MyEssentialApp" "dbo" "SessionData"

# Blazor
dotnet new -i Microsoft.AspNetCore.Blazor.Templates::3.0.0-preview9.19465.2
dotnet new blazorwasm -o BlazorApp
dotnet watch run --urls=https://127.0.0.1:5500


## navigate https://127.0.0.1:5500

System.Console.WriteLine("Counter: " + currentCount);

restart

# Blazor server
<base href="/blazor/" />

dotnet add package Microsoft.AspNetCore.Blazor.Server --version 3.0.0-preview9.19465.2
dotnet add reference ..\BlazorApp

now blazor response
https://localhost:5001/blazor
and not https://127.0.0.1:5500

# Displaying Blazor Components in an MVC Razor View

# Using Angular and Blazor in the Same View

bug hidden. I had to undo the pending changes and restart from scratch. The issue