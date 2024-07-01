# Build Pipeline Process for .Net8.0 in Azure Devops Organization

1. dotnet sdk installation
2. dotnet restore 
3. dotnet build
4. dotnet publish 
5. nuget pack
6. generate nuspec
7. push to azure artifacts


# Release Pipeline Process for .Net8.0 in Azure Devops Organization

1. artifact selection from the azure artifacts
2. define a stage to deploy the artifact to a function app