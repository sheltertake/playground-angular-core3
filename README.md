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