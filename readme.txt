dotnet new webapi -o dotnetDemo1
dotnet run (in development mode)

# publish build in release (production mode)
# run this command to generate production build files 
# UseAppHost=true : to generate exe file - you start the app from the exe file direct
# UseAppHost=false : to generate dll file - you must start via "dotnet <project.dll>"

dotnet publish -c Release -o ./publish /p:UseAppHost=true
dotnet publish -c Release -o ./publish /p:UseAppHost=false

# set running port in production
export ASPNETCORE_URLS=http://+:8081
set ASPNETCORE_URLS=http://+:8081

# run the execution file
publish/backend  