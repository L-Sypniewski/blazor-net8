# A project to play around with NET 8 Blazor

## Template used

```sh
dotnet new blazor -n BlazorDotnetEight -int Auto -au None
```

## Build docker image locally

```sh
dotnet publish BlazorDotnetEight/BlazorDotnetEight/BlazorDotnetEight.csproj  -p:PublishProfile=BlazorDotnetEight/BlazorDotnetEight/Properties/PublishProfiles/local.pubxml -c Release 
```

## Build docker image to Github Packages

```sh
dotnet publish BlazorDotnetEight/BlazorDotnetEight/BlazorDotnetEight.csproj  -p:PublishProfile=BlazorDotnetEight/BlazorDotnetEight/Properties/PublishProfiles/github.pubxml -c Release 
```

## Run locally build docker image

```sh
docker run -d --name blazor-dotnet-eight-webapi-dev -p 5000:8080 -e ASPNETCORE_ENVIRONMENT=Development -u app blazor-dotnet-eight-image:dev
```
