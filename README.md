# Build Pipeline Process for .Net8.0 in Azure Devops Organization

## dotnet sdk installation
* Install dotnet sdk with version 6.x or 8.x

## dotnet restore 
* dotnet restore - Restores the dependencies and tools of a project.
* We can restore csproj or solution file 
* We can define nuget.config with package configurations or 
* Select the feed in specific organization
* You can use packages from nuget.org

## dotnet build
* dotnet build - Builds a project and all of its dependencies.
> dotnet build *.csproj/.sln --configuration Debug/Release --output filename --runtime win-x86

## dotnet publish 
* dotnet publish - Publishes the application and its dependencies to a folder for deployment to a hosting system.
> dotnet publish *.csproj/.sln --configuration Debug/Release 

## nuget pack or dotnet pack 
> dotnet pack - Packs the code into a NuGet package. Requires csproj 

> nuget pack - Packs the code into a NuGet package. Requires nuspec file with all the dependencies from csproj(package references)

* The above commands will generate a .nupkg file which is the artifact pushed to the azure artifacts and can be used for deployment to a hosting system

## push to azure artifacts
> dotnet nuget push *.nupkg -k|--api-key <API_KEY> -s|--source <SOURCE>

# Release Pipeline Process for .Net8.0 in Azure Devops Organization

1. artifact selection from the azure artifacts
2. define a stage to deploy the artifact to a function app














